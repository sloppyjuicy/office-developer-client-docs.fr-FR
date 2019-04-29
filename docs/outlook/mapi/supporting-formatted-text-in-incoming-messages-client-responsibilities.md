---
title: Prise en charge du texte mis en forme dans les messages entrants responsabilités du client
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434500"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Prise en charge du texte mis en forme dans les messages entrants: responsabilités du client

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque les messages sont transférés entre les systèmes de messagerie, le spouleur MAPI garantit que la mise en forme de texte enrichi reste synchronisée avec le texte du message. Le spouleur MAPI appelle la fonction [RTFSync](rtfsync.md) à partir d'une version encapsulée du message qu'il transmet au fournisseur de transport. Le fournisseur de transport enregistre les modifications apportées au message en appelant la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , puis l'achemine vers le nouveau destinataire. 
  
Lorsque l'application cliente compatible RTF du destinataire ouvre le message pour afficher le texte, elle doit synchroniser le texte avec la mise en forme et ouvrir **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , en fonction de la disponibilité de la propriété.
  
 **Pour ouvrir un message, les clients compatibles RTF**
  
1. Appelez **RTFSync** pour synchroniser le texte du message avec la mise en forme si la Banque de messages n'est pas compatible avec le format RTF. L'indicateur RTF_SYNC_BODY_CHANGED doit être passé dans le paramètre _ulFlags_ si la propriété **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) est MANQUante ou a la valeur false. Les clients qui travaillent avec des banques de messages compatibles RTF n'ont pas besoin d'effectuer l'appel **RTFSync** , car la Banque de messages s'en charge. 
    
2. Appelez [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) si le texte du message a été mis à jour. 
    
3. Appelez [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED** . Si **PR_RTF_COMPRESSED** n'est pas disponible, vous devez ouvrir la propriété **PR_BODY** à la place pour afficher le contenu du message. 
    
4. Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) pour créer une version non compressée des données RTF compressées, le cas échéant. 
    
5. Afficher les données RTF non compressées ou les données en texte brut à l'utilisateur.
    
 **RTFSync** renvoie une valeur de type Boolean qui indique si le message a été mis à jour ou non. Si cette valeur retourne la valeur TRUE, appelez **SaveChanges** à un moment donné pour faire en sorte que la mise à jour soit définitive. L'appel ne doit pas être effectué immédiatement après le retour de **RTFSync** . 
  
> [!NOTE]
> Étant donné que de nombreux composants gèrent le texte mis en forme avant que vous ne le receviez, il existe un risque d'endommagement. Cette altération peut provenir du fournisseur de banque de messages, d'une application tierce, d'une passerelle ou d'une erreur de transmission. 
  

