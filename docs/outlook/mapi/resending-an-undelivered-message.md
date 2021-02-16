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
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432666"
---
# <a name="resending-an-undelivered-message"></a>Renvoi d’un message non remis
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur de transport envoie une rapport de non-remise (NDR) lorsqu’il ne peut pas remettre correctement un message que vous avez envoyé. C’est au client de décider si les utilisateurs peuvent tenter de renvoyer ces messages non envoyés. Si vous vous chargez de renvoyer des messages, vous pouvez utiliser un formulaire fourni par MAPI ou implémenter le vôtre. Le formulaire MAPI affiche les noms des destinataires en échec et la raison de l’échec de remise, si possible, et inclut un bouton qui, lorsqu’il est sélectionné, permet à un utilisateur de renvoyer le message.
  
Lorsqu’un message de nouvelle réception est reçu, il doit ressembler exactement au message d’origine. Le destinataire ne doit pas être en mesure de différencier un message remis lors de sa première tentative de transmission ou d’une tentative ultérieure. Les réponses à ce message doivent fonctionner exactement comme si le message avait été envoyé avec succès la première fois.
  
### <a name="to-resend-an-undelivered-message"></a>Pour renvoyer un message non reçu
  
1. Appelez [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) pour créer un message. 
    
2. Copiez toutes les propriétés du message d’origine, à l’exception de la propriété ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), et des propriétés **PR_SENDER** et **PR_SENT_REPRESENTING.** A effectuer les modifications de propriété suivantes : 
    
   - Définissez **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) à la propriété **PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) de l’état.
    
   - Définissez MSGFLAG_RESEND’indicateur **de** PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
    
   - Définissez **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) sur la propriété PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)) du message d’origine.
    
   - Pour chaque destinataire, définissez MAPI_SUBMITTED la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). 
    
   - Dupliquer chaque destinataire en échec. Modifiez **la PR_RECIPIENT_TYPE** du destinataire dupliqué en MAPI_P1. Par conséquent, pour chaque destinataire ayant échoué, il existe désormais deux entrées dans la table  des destinataires : une avec **PR_RECIPIENT_TYPE** définie sur sa valeur d’origine et l’autre avec PR_RECIPIENT_TYPE définie sur MAPI_P1. 
    
3. Appelez [ScCreateConversationIndex](sccreateconversationindex.md) pour configurer le suivi des conversations si vous le souhaitez. 
    
4. Appelez la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) du nouveau message pour mettre à jour la liste des destinataires. 
    
5. Appelez [IMessage::SubmitMessage](imessage-submitmessage.md) pour enregistrer et envoyer le nouveau message. 
    

