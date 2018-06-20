---
title: Envoyer des Messages à l’aide de traitement des pièces jointes personnalisé TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 1dae8d3a7830ddbc50176ec09415457ca9fdac23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787104"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>Envoyer des Messages à l’aide de traitement des pièces jointes personnalisé TNEF

 
  
**S’applique à**: Outlook 
  
Pour personnaliser le traitement des pièces jointes lors de l’envoi d’un message :
  
1. Obtenir un objet TNEF en passant une interface **IStream** et un message dans la fonction [OpenTnefStreamEx](opentnefstreamex.md) . 
    
2. Pour obtenir une liste de toutes les propriétés définies pour le message en appelant la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
    
3. Utilisez les méthodes [IMAPIProp](imapipropiunknown.md) pour exclure toutes les propriétés prises en charge par le système de messagerie. À un moment opportun écrire ces propriétés dans le système de messagerie dans le format requis par le système de messagerie. 
    
4. Appelez la méthode [ITnef::AddProps](itnef-addprops.md) pour ajouter uniquement les propriétés sur le message — autrement dit, aucune des propriétés sur les pièces jointes, en définissant l’indicateur TNEF_PROP_MESSAGE_ONLY. 
    
5. Appelez [ITnef::AddProps](itnef-addprops.md) avec ces éléments : l’indicateur TNEF_PROP_EXCLUDE, un tableau de balise de propriété qui contient le **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) propriété et un identificateur de pièce jointe qui spécifie la pièce jointe à traiter.
    
6. Utilisez la méthode [ITnef::SetProps](itnef-setprops.md) pour ajouter la balise de propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) avec une chaîne unique qui identifie le système de messagerie de la pièce jointe si la pièce jointe comporte un nom de fichier que le système de messagerie ne peut pas prendre en charge. Par exemple, plusieurs pièces jointes avec le même nom de fichier d’origine, ou un nom de fichier qui n’est pas un nom de fichier valide pour le système de messagerie. Cette chaîne est utilisée avec un numéro de clé lorsque vous écrivez les balises de pièce jointe dans le texte du message avec balise pour associer une pièce jointe à ses données. Pour plus d’informations, voir [TNEF-Tagged le texte du Message](tnef-tagged-message-text.md).
    
7. Répétez les appels **AddProps** et **SetProps** pour chaque pièce jointe. 
    
8. Appelez la méthode [ITnef::Finish](itnef-finish.md) pour coder le message dans le flux TNEF après avoir ajouté toutes les propriétés demandées. 
    
9. Obtenir le texte du message avec balise en appelant la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) . Ce texte référencé est en lecture à l’aide des méthodes de l’interface **IStream** , codé à l’aide du modèle de pièce jointe du système de messagerie et écrites dans le système de messagerie. 
    
10. Appelez la méthode [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) pour libérer de l’objet [ITnef](itnefiunknown.md) . 
    
11. Écrire des pièces jointes restants sur le système de messagerie via le modèle de pièce jointe du système de messagerie.
    
Votre fournisseur de transport doit utiliser la procédure décrite précédemment aux pièces jointes des processus. Si ce n’est pas possible, le fournisseur de transport doit utiliser les étapes suivantes pour le traitement personnalisé des pièces jointes :
  
1. Le fournisseur de transport garantit que les propriétés **PR_ATTACH_TRANSPORT_NAME** de toutes les pièces jointes contiennent des valeurs uniques sont des identificateurs de pièce jointe valide pour le système de messagerie. 
    
2. Le fournisseur de transport utilise un seul appel à **ITnef::AddProps** pour chaque pièce jointe, en passant l’indicateur TNEF_PROP_CONTAINED. 
    

