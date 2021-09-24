---
title: Envoi de messages à l’aide de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c54271a24f149ef459b5646022b23823e4fbc1c4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550056"
---
# <a name="sending-messages-by-using-mapi"></a>Envoi de messages à l’aide de MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes [appellent la méthode IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer un message. **SubmitMessage** appelle [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour enregistrer le message avant de transférer le contrôle vers lepooler MAPI ou directement vers un fournisseur de transport. 
  
Lepooler MAPI reçoit le message si l’une des erreurs suivantes se produit :
  
- Le fournisseur de magasins de messages et le fournisseur de transport ne sont pas étroitement associés.
    
- Le message nécessite un prétraitment.
    
- La boutique de messages et le transport étroitement couplés ne peuvent pas gérer tous les destinataires auxquels le message est adressé.
    
Une banque de messages étroitement couplée doit prendre en compte l’état d’un message avant de le présenter aupooler MAPI à télécharger vers un fournisseur de transport. Il existe des situations dans lesquelles un message peut sembler nécessiter lepooler MAPI, mais lepooler MAPI ne doit vraiment pas être impliqué.
  
Par exemple, considérez la situation dans laquelle un utilisateur envoie un message à partir de la boîte de réception. Le client utilise un magasin et un transport étroitement couplés. Si la magasin de messages étroitement couplé utilise l’emplacement du message comme seul critère pour décider si lepooler MAPI peut ou non gérer le message, lepooler MAPI reçoit toujours le message. Pour éviter ce type de problème, une magasin de messages étroitement couplé doit vérifier l’état du message en plus de l’emplacement du message. Plus précisément, le fournisseur de transport ne doit pas demander aupooler MAPI de télécharger les messages soumis activement.
  
Le processus de transmission des messages implique le fournisseur de la boutique de messages, un ou plusieurs fournisseurs de transport et MAPI. Les rubriques de cette section fournissent des informations détaillées sur des rôles spécifiques dans le processus de transmission de message.
  
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

