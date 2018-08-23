---
title: Renvoi d’un message non remis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cdb1ef3cf6db2a1b63b68a105867aa6624b80c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588894"
---
# <a name="resending-an-undelivered-message"></a>Renvoi d’un message non remis
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un fournisseur de transport envoie un rapport de non-remise (NDR) lorsqu’il ne peut pas remettre avec succès un message que vous avez soumis. C’est le client ou non les utilisateurs peuvent tenter de renvoyer ces messages non remis. Si vous prenez en charge le renvoi de messages, vous pouvez utiliser un formulaire fourni par MAPI ou implémenter votre propre. Le formulaire MAPI affiche les noms des destinataires ayant échoués et la raison de l’échec de remise, dans la mesure du possible et inclut un bouton qui, lorsque sélectionnée, permet à un utilisateur de renvoyer le message.
  
Lorsqu’un message récente est reçu, il doit se présenter exactement comme le message d’origine. Le destinataire doit être impossible de faire la distinction entre un message qui a été remis sur sa première tentative de transmission ou d’une nouvelle tentative. Réponses de ce message devraient fonctionner comme si le message a été envoyé correctement la première fois.
  
### <a name="to-resend-an-undelivered-message"></a>Pour renvoyer un message non remis
  
1. Appelez [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer un nouveau message. 
    
2. Copier toutes les propriétés à partir du message d’origine, à l’exclusion de la ** PR_MESSAGE_RECIPIENTS **, propriété ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) et les propriétés **PR_SENDER** et **PR_SENT_REPRESENTING** . Apportez les modifications de propriété suivantes : 
    
   - La valeur de l’état **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) ** PR_ORIG_MESSAGE_CLASS ** propriété ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)).
    
   - Définir l’indicateur MSGFLAG_RESEND dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
   - La valeur **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du message d’origine.
    
   - Pour chaque destinataire, définissez MAPI_SUBMITTED dans la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). 
    
   - En double chaque destinataire ayant échoué. Modifier la propriété **PR_RECIPIENT_TYPE** pour le destinataire dupliqué à MAPI_P1. Par conséquent, pour chaque destinataire ayant échoué il existe maintenant deux entrées dans la table de destinataires : une avec **PR_RECIPIENT_TYPE** défini à sa valeur d’origine et l’autre avec **PR_RECIPIENT_TYPE** défini à MAPI_P1. 
    
3. Appelez [ScCreateConversationIndex](sccreateconversationindex.md) pour configurer la conversation si vous le souhaitez. 
    
4. Appeler la méthode de [IMessage::ModifyRecipients](imessage-modifyrecipients.md) du nouveau message pour mettre à jour la liste des destinataires. 
    
5. Appelez [IMessage::SubmitMessage](imessage-submitmessage.md) pour enregistrer et envoyer le nouveau message. 
    

