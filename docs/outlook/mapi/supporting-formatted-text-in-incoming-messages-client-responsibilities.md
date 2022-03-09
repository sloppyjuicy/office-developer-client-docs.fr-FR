---
title: Prise en charge du texte formaté dans les responsabilités du client des messages entrants
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
ms.openlocfilehash: 2b0ffb5dde153f6cf2fa89624de96e68af82bb4c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371190"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Prise en charge du texte formaté dans les messages entrants : responsabilités du client

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque les messages sont transférés entre les systèmes de messagerie, lepooler MAPI s’assure que la mise en forme de texte enrichi reste synchronisée avec le texte du message. Lepooler MAPI appelle la [fonction RTFSync](rtfsync.md) à partir d’une version wrapped du message qu’il transmet au fournisseur de transport. Le fournisseur de transport enregistre les modifications apportées au message en appelant la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , puis l’a acheminé vers le nouveau destinataire. 
  
Lorsque l’application cliente RTF du destinataire ouvre le message pour afficher le texte, elle doit synchroniser le texte avec la mise en forme et ouvrir **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), en fonction de la propriété disponible.
  
 **Pour ouvrir un message, clients rtF**
  
1. Appelez **RTFSync pour** synchroniser le texte du message avec la mise en forme si la boutique de messages n’est pas sensible au format RTF. L’RTF_SYNC_BODY_CHANGED doit être transmis dans le paramètre _ulFlags_ si la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) est manquante ou définie sur FALSE. Les clients qui travaillent avec des magasins de messages rtF n’ont pas besoin d’effectuer l’appel **RTFSync** , car la boutique de messages s’en charge. 
    
2. [Appelez IMAPIProp::SaveChanges](imapiprop-savechanges.md) si le texte du message a été mis à jour. 
    
3. [Appelez IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir **PR_RTF_COMPRESSED propriété.** Si **PR_RTF_COMPRESSED** n’est pas disponible, vous devez ouvrir la **propriété PR_BODY** à la place pour afficher le contenu du message. 
    
4. Appelez la [fonction WrapCompressedRTFStream](wrapcompressedrtfstream.md) pour créer une version non compressée des données RTF compressées, si disponible. 
    
5. Affichez les données RTF non compressées ou les données en texte simple à l’utilisateur.
    
 **RTFSync renvoie** une valeur boolé américaine qui indique si le message a été mis à jour ou non. Si cette valeur renvoie TRUE, appelez **SaveChanges** à un moment donné pour rendre la mise à jour permanente. L’appel n’a pas besoin d’être effectué immédiatement après le **retour de RTFSync** . 
  
> [!NOTE]
> Étant donné que de nombreux composants gèrent le texte formaté avant de le recevoir, il existe un risque d’altération. Cette altération peut être le fait du fournisseur de la boutique de messages, d’une application tierce, d’une passerelle ou d’une erreur de transmission. 
  

