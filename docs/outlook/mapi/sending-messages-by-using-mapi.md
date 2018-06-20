---
title: Envoyer des Messages à l’aide de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 36de3b70b0ab7b16f8abed85bbd0983224e00568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787112"
---
# <a name="sending-messages-by-using-mapi"></a>Envoyer des Messages à l’aide de MAPI

  
  
**S’applique à**: Outlook 
  
Applications clientes appellent la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) pour envoyer un message. **SubmitMessage** appelle [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour enregistrer le message avant de transférer le contrôle soit le spouleur MAPI ou directement à un fournisseur de transport. 
  
Le spouleur MAPI reçoit le message si une des actions suivantes se produisent :
  
- Le fournisseur de banque de message et le fournisseur de transport ne sont pas étroitement liées.
    
- Le message nécessite un prétraitement.
    
- La banque de messages étroitement couplés et de transport ne peut pas gérer tous les destinataires auxquels le message est adressé.
    
Une banque de messages étroitement couplés doit prendre en considération état d’un message avant qu’il présente le spouleur MAPI à transférer vers un fournisseur de transport. Il existe des situations où un message s’affiche pour demander le spouleur MAPI, mais le spouleur MAPI doit vraiment pas impliqué.
  
Par exemple, considérez la situation où un utilisateur envoie un message à partir de la boîte de réception. Le client utilise un magasin étroitement couplé et transport. Si la banque de messages étroitement couplés utilise l’emplacement du message comme critère unique permettant de décider s’il faut autoriser le spouleur MAPI sur les gérer le message, le spouleur MAPI toujours le message. Pour éviter ce type de problème, une banque de messages étroitement couplés doit vérifier le statut du message en plus de l’emplacement du message. Plus précisément, le fournisseur de transport ne doit pas demander que le spouleur MAPI télécharger tout message est envoyé en.
  
Le processus de transmission de message implique le fournisseur de banque de message, un ou plusieurs fournisseurs de transport et MAPI. Les rubriques de cette section fournissent des informations détaillées sur des rôles spécifiques dans le processus de transmission de message.
  
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

