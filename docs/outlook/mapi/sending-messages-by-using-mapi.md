---
title: Envoi de messages à l'aide de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438721"
---
# <a name="sending-messages-by-using-mapi"></a>Envoi de messages à l'aide de MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes appellent la méthode [IMessage:: SubmitMessage](imessage-submitmessage.md) pour envoyer un message. **SubmitMessage** appelle [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) pour enregistrer le message avant de transférer le contrôle vers le spouleur MAPI ou directement vers un fournisseur de transport. 
  
Le spouleur MAPI reçoit le message si l'un des éléments suivants se produit:
  
- Le fournisseur de banque de messages et le fournisseur de transport ne sont pas étroitement couplés.
    
- Le message doit être prétraité.
    
- La Banque de messages et le transport étroitement couplés ne peuvent pas gérer tous les destinataires auxquels le message est adressé.
    
Un magasin de messages étroitement couplé doit prendre en compte l'état d'un message avant de le présenter au spouleur MAPI afin d'être téléchargé vers un fournisseur de transport. Il existe des situations dans lesquelles un message peut sembler exiger le spouleur MAPI, mais le spouleur MAPI ne doit pas être impliqué.
  
Par exemple, considérez la situation dans laquelle un utilisateur envoie un message à partir de la boîte de réception. Le client utilise un magasin et un transport étroitement couplés. Si la Banque de messages étroitement couplée utilise l'emplacement du message comme critère unique pour décider d'autoriser ou non le spouleur MAPI à gérer le message, le spouleur MAPI reçoit toujours le message. Pour éviter ce type de problème, un magasin de messages étroitement couplé doit vérifier l'état du message en plus de l'emplacement du message. Plus précisément, le fournisseur de transport ne doit pas demander au spouleur MAPI de télécharger les messages soumis activement.
  
Le processus de transmission de messages implique le fournisseur de banque de messages, un ou plusieurs fournisseurs de transport et MAPI. Les rubriques de cette section fournissent des informations détaillées sur des rôles spécifiques dans le processus de transmission des messages.
  
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

