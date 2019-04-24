---
title: Envoi de messages à l'aide du traitement des pièces jointes personnalisé TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339696"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>Envoi de messages à l'aide du traitement des pièces jointes personnalisé TNEF

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour personnaliser le traitement des pièces jointes lors de l'envoi d'un message:
  
1. Obtenez un objet TNEF en transmettant une interface **IStream** et un message dans la fonction [OpenTnefStreamEx](opentnefstreamex.md) . 
    
2. Obtenir la liste de toutes les propriétés définies pour le message en appelant la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) . 
    
3. Utilisez les méthodes [IMAPIProp](imapipropiunknown.md) pour exclure toutes les propriétés prises en charge par le système de messagerie. À un moment approprié, écrivez ces propriétés dans le système de messagerie au format requis par le système de messagerie. 
    
4. Appelez la méthode [ITnef:: AddProps](itnef-addprops.md) pour ajouter uniquement les propriétés du message, c'est-à-dire aucune des propriétés des pièces jointes, en définissant l'indicateur TNEF_PROP_MESSAGE_ONLY. 
    
5. Appelez [ITnef:: AddProps](itnef-addprops.md) avec ces éléments: l'indicateur TNEF_PROP_EXCLUDE, un tableau de balises de propriété qui contient les **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) propriété et un identificateur de pièce jointe qui spécifie la pièce jointe à traiter.
    
6. Utilisez la méthode [ITnef:: SetProps](itnef-setprops.md) pour ajouter la balise de propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) avec une chaîne unique qui identifie la pièce jointe au système de messagerie si la pièce jointe possède un nom de fichier que le paramètre le système de messagerie ne prend pas en charge. Par exemple, plusieurs pièces jointes avec le même nom de fichier d'origine, ou un nom de fichier qui n'est pas un nom de fichier valide pour le système de messagerie. Cette chaîne sera utilisée avec un numéro de clé lors de l'écriture des balises de pièces jointes dans le texte du message balisé afin d'associer une pièce jointe à ses données. Pour plus d'informations, reportez-vous à la rubrique [texte du message avec balisAge TNEF](tnef-tagged-message-text.md).
    
7. Répétez les appels **AddProps** et **SetProps** pour chaque pièce jointe. 
    
8. Appelez la méthode [ITnef:: Finish](itnef-finish.md) pour coder le message dans le flux TNEF une fois toutes les propriétés demandées ajoutées. 
    
9. Obtenez le texte du message balisé en appelant la méthode [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) . Ce texte balisé est lu à l'aide des méthodes de l'interface **IStream** , codée à l'aide du modèle de pièce jointe du système de messagerie, et écrite dans le système de messagerie. 
    
10. Appelez la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) pour libérer l'objet [ITnef](itnefiunknown.md) . 
    
11. Écrivez les pièces jointes restantes dans le système de messagerie via le modèle de pièces jointes du système de messagerie.
    
Votre fournisseur de transport doit utiliser la procédure décrite précédemment pour traiter les pièces jointes. Si cela n'est pas possible, le fournisseur de transport doit utiliser les étapes suivantes pour le traitement des pièces jointes personnalisées:
  
1. Le fournisseur de transport garantit que les propriétés **PR_ATTACH_TRANSPORT_NAME** de toutes les pièces jointes contiennent des valeurs uniques qui correspondent à des identificateurs de pièces jointes valides pour le système de messagerie. 
    
2. Le fournisseur de transport utilise ensuite un seul appel à **ITnef:: AddProps** pour chaque pièce jointe, en transmettant l'indicateur TNEF_PROP_CONTAINED. 
    

