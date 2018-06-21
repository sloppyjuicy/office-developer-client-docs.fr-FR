---
title: Prise en charge de mise en forme le texte dans les responsabilités du Client les Messages entrants
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 863c95856f3198c74bb9d72881154676386f6a9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19787292"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Prise en charge au format texte dans les Messages entrants : responsabilités du Client

  
  
**S’applique à**: Outlook 
  
Les messages sont transférés entre les systèmes de messagerie, le spouleur MAPI permet de garantir que la mise en forme de texte enrichi reste synchronisé avec le texte du message. Le spouleur MAPI appelle la fonction [RTFSync](rtfsync.md) dans une version encapsulée du message qu’il passe au fournisseur de transport. Le fournisseur de transport enregistre les modifications apportées au message en appelant la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , puis l’achemine vers le nouveau destinataire. 
  
Lors de l’application cliente prenant en charge les RTF du destinataire ouvre le message pour afficher le texte, il doit synchroniser le texte avec la mise en forme et ouvrez **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , en fonction de la propriété qui est disponible.
  
 **Pour ouvrir un message, les clients prenant en charge au format RTF**
  
1. Appelez **RTFSync** pour synchroniser le texte du message avec la mise en forme si la banque de messages n’est pas en charge au format RTF. L’indicateur RTF_SYNC_BODY_CHANGED doit être passé dans le paramètre _ulFlags_ si la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) est manquante ou la valeur FALSE. Utilisation des banques de messages RTF prenant en charge les clients ne doivent pas d’appeler le **RTFSync** car la banque de messages prend en charge de celle-ci. 
    
2. Appeler [IMAPIProp::SaveChanges](imapiprop-savechanges.md) si le texte du message a été mis à jour. 
    
3. Appelez [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED** . Si **PR_RTF_COMPRESSED** n’est pas disponible, vous devez ouvrir la propriété **PR_BODY** à la place pour afficher le contenu du message. 
    
4. Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) pour créer une version non compressée des données au format RTF compressées, si elle est disponible. 
    
5. Afficher les données de texte brut ou des données au format RTF décompressées à l’utilisateur.
    
 **RTFSync** renvoie une valeur de type Boolean qui indique si le message a été mis à jour. Si cette valeur renvoie la valeur TRUE, appelez **SaveChanges** à un moment donné pour conserver la mise à jour. L’appel n’a pas immédiatement après que renvoie **RTFSync** . 
  
> [!NOTE]
> Car c’est le cas de nombreux composants gèrent le texte mis en forme avant sa réception, il est possible de corruption. Cela peut provenir le fournisseur de banque de messages, une application tierce, une passerelle ou une erreur de transmission. 
  

