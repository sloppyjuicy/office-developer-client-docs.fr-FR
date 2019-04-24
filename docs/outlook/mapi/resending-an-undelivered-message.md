---
title: Renvoi d’un message non remis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328678"
---
# <a name="resending-an-undelivered-message"></a>Renvoi d’un message non remis
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur de transport envoie une notification d'échec de remise lorsqu'il ne parvient pas à remettre un message que vous avez envoyé. Il revient au client si les utilisateurs peuvent essayer de renvoyer ces messages non remis. Si vous prenez en charge la retransmission des messages, vous pouvez soit utiliser un formulaire fourni par MAPI, soit implémenter votre propre message. Le formulaire MAPI affiche les noms des destinataires ayant échoué et la raison de l'échec de remise, si possible, et inclut un bouton qui, lorsqu'il est sélectionné, permet à un utilisateur de renvoyer le message.
  
Lorsqu'un message renvoyé est reçu, il doit ressembler exactement au message d'origine. Le destinataire ne doit pas faire la différence entre un message qui a été remis lors de sa première tentative de transmission ou une tentative ultérieure. Les réponses sur ce message doivent fonctionner exactement comme si le message avait été envoyé avec succès la première fois.
  
### <a name="to-resend-an-undelivered-message"></a>Pour renvoyer un message non remis
  
1. Appelez [IMAPIFolder: CreateMessage](imapifolder-createmessage.md) pour créer un message. 
    
2. Copiez toutes les propriétés du message d'origine, à l'exception de la propriété * * PR_MESSAGE_RECIPIENTS * * ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), ainsi que les propriétés **PR_SENDER** et **PR_SENT_REPRESENTING** . Effectuez les modifications de propriétés suivantes: 
    
   - Définissez **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) sur la propriété * * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) de l'État.
    
   - Définissez l'indicateur MSGFLAG_RESEND dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
   - Définissez **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) sur la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du message d'origine.
    
   - Pour chaque destinataire, définissez MAPI_SUBMITTED dans la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). 
    
   - Dupliquez chaque destinataire ayant échoué. Modifiez la propriété **PR_RECIPIENT_TYPE** pour le destinataire DUPLIQUÉ vers MAPI_P1. Par conséquent, pour chaque destinataire ayant échoué, il y a maintenant deux entrées dans la table des destinataires: une avec **PR_RECIPIENT_TYPE** définie à sa valeur d'origine et l'autre avec **PR_RECIPIENT_TYPE** défini sur MAPI_P1. 
    
3. Appelez [ScCreateConversationIndex](sccreateconversationindex.md) pour configurer le suivi des conversations si vous le souhaitez. 
    
4. Appelez la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) du nouveau message pour mettre à jour la liste des destinataires. 
    
5. Appelez [IMessage:: SubmitMessage](imessage-submitmessage.md) pour enregistrer et envoyer le nouveau message. 
    

