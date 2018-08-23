---
title: Envoi d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6845c3d86fb3d34119a296ebbae76a7322d7d8c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590910"
---
# <a name="sending-a-message"></a>Envoi d’un message

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsque vous êtes prêt à envoyer un message, appelez la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) . **SubmitMessage** place le message dans la file d’attente sortant et définit l’indicateur MSGFLAG_SUBMIT dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message.
  
Le fournisseur de banque de messages, si étroitement lié à un fournisseur de transport, donne le message directement vers le transport qui transmet au système de messagerie. Si ce n’est pas étroitement couplés, le fournisseur de banque de message informe le spouleur MAPI que la file d’attente sortant a été modifié et le spouleur MAPI transfère le message vers un fournisseur de transport approprié.
  
Si vous autorisez les utilisateurs d’annuler une opération d’envoi, appelez [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) pour implémenter cette fonctionnalité. **AbortSubmit** supprime le message de la file d’attente sortante. Les utilisateurs peuvent être autorisés à arrêter un envoi de se produire jusqu'à ce que le message est affecté au système de messagerie sous-jacent. 
  
Si **SubmitMessage** renvoie MAPI_E_CORRUPT_DATA, partent du principe que les données envoyées sont maintenant perdu. Avant d’essayer d’envoyer une deuxième fois, réécrire le message en appelant [IMAPIProp::SetProps](imapiprop-setprops.md) et [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Afficher une erreur à l’utilisateur si ces appels **IMAPIProp** échouent ou si **SubmitMessage** échoue une deuxième fois. 
  
Après un appel réussi à **SubmitMessage**, libérer de la mémoire allouée pour la liste de destinataires et libérer le message et ses pièces jointes. Une fois qu’un message a été envoyé, MAPI n’autorise pas les autres opérations sur les pointeurs pour ces objets. La seule exception appelle **IUnknown::Release**. Aucun autre appel n’est autorisés, car de nombreux fournisseurs de banque de message invalident les identificateurs d’entrée pour les messages qui ont été envoyés.
  

