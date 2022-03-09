---
title: Envoi de messages à l’aide de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
ms.openlocfilehash: f5b63c6c73b58b4e7ed67ceb6a67245bdfbe4cb1
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376089"
---
# <a name="sending-messages-by-using-mapi"></a>Envoi de messages à l’aide de MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes [appellent la méthode IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer un message. **SubmitMessage** appelle [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour enregistrer le message avant de transférer le contrôle vers lepooler MAPI ou directement vers un fournisseur de transport. 
  
Lepooler MAPI reçoit le message si l’une des erreurs suivantes se produit :
  
- Le fournisseur de magasin de messages et le fournisseur de transport ne sont pas étroitement associés.
    
- Le message nécessite un prétraitment.
    
- La boutique de messages et le transport étroitement couplés ne peuvent pas gérer tous les destinataires auxquels le message est adressé.
    
Une banque de messages étroitement couplée doit prendre en compte l’état d’un message avant de le présenter aupooler MAPI à télécharger vers un fournisseur de transport. Il existe des situations dans lesquelles un message peut sembler nécessiter lepooler MAPI, mais lepooler MAPI ne doit vraiment pas être impliqué.
  
Par exemple, prenons la situation dans laquelle un utilisateur envoie un message à partir de la boîte de réception. Le client utilise un magasin et un transport étroitement couplés. Si la magasin de messages étroitement couplé utilise l’emplacement du message comme seul critère pour décider si lepooler MAPI peut ou non gérer le message, lepooler MAPI reçoit toujours le message. Pour éviter ce type de problème, une magasin de messages étroitement couplé doit vérifier l’état du message en plus de l’emplacement du message. Plus précisément, le fournisseur de transport ne doit pas demander aupooler MAPI de télécharger les messages soumis activement.
  
Le processus de transmission de message implique le fournisseur de magasins de messages, un ou plusieurs fournisseurs de transport et MAPI. Les rubriques de cette section fournissent des informations détaillées sur des rôles spécifiques dans le processus de transmission de message.
  
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

