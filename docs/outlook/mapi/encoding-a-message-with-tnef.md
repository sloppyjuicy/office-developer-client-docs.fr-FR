---
title: Codage d’un message avec TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382525"
---
# <a name="encoding-a-message-with-tnef"></a>Codage d’un message avec TNEF

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un message est envoyé, le fournisseur de transport peut créer un fichier qui est utilisé pour contenir le message lors de la transmission. Ensuite, une interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) est autour du fichier. Le fournisseur de transport utilise ensuite les méthodes [ITnef](itnefiunknown.md) pour écrire les propriétés de message dans le flux dans un format avec balise qui permet les propriétés à décoder facilement par les fournisseurs de transport de réception. 
  
**Pour représenter un message dans un seul fichier entier**
  
1. Obtenir un objet TNEF en passant un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) et un message dans la fonction [OpenTnefStreamEx](opentnefstreamex.md) . 
    
2. Pour obtenir une liste de toutes les propriétés définies pour le message en appelant la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
    
3. Utilisez les méthodes [IMAPIProp](imapipropiunknown.md) pour exclure toutes les propriétés prises en charge par le système de messagerie. À un moment opportun, écrire ces propriétés dans le système de messagerie dans le format requis par le système de messagerie. 
    
4. Appelez [ITnef::AddProps](itnef-addprops.md) pour coder les propriétés restantes, y compris toutes les pièces jointes. 
    
5. Appelez la méthode [ITnef::Finish](itnef-finish.md) pour coder le message dans le flux TNEF après avoir ajouté toutes les propriétés demandées. 
    
6. Appelez la méthode [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) pour obtenir le texte du message avec balise. Ce texte balisé est écrites dans le système de messagerie à l’aide des méthodes de l’interface OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . 
    
7. Appelez la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) pour libérer de l’objet **ITnef** . 
    
**Pour traiter un message TNEF entrant**
  
1. Obtenir un objet de message MAPI dans le spouleur MAPI et écrire des propriétés d’en-tête de message dans le nouveau message MAPI.
    
2. Créer et initialiser un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) pour contenir les données TNEF à partir du message entrant. 
    
3. Transmettre le message MAPI et l’objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) à la fonction [OpenTnefStreamEx](opentnefstreamex.md) . 
    
4. Décoder les informations contenues dans les données TNEF en appelant la méthode [ITnef::ExtractProps](itnef-extractprops.md) . 
    
   > [!NOTE]
   > Rien décodé par **ExtractProps** remplacera les propriétés décodées à partir de l’enveloppe du message entrant. Autrement dit, les propriétés extraites TNEF remplacera les propriétés existantes dans un message. 
  
5. Traiter le texte du message avec balise en appelant [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) et analysez le texte pour récupérer les positions des pièces jointes. 
    
6. Enregistrez le message en appelant [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
7. Version de l’objet TNEF en appelant la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) . 
    

