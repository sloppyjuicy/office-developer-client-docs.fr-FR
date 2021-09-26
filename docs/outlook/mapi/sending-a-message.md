---
title: Envoi d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 291d1b5595c8f0779b5d5644397a1ebfd2576a0f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629584"
---
# <a name="sending-a-message"></a>Envoi d’un message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous êtes prêt à envoyer un message, appelez sa [méthode IMessage::SubmitMessage.](imessage-submitmessage.md) **SubmitMessage** place le message dans la file d’attente sortante et définit l’indicateur MSGFLAG_SUBMIT dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message.
  
Le fournisseur de magasins de messages, s’il est étroitement associé à un fournisseur de transport, fournit le message directement au transport qui le remet au système de messagerie. S’il n’est pas étroitement couplé, le fournisseur de magasins de messages informe lepooler MAPI que la file d’attente sortante a changé et que lepooler MAPI transfère le message à un fournisseur de transport approprié.
  
Si vous autorisez les utilisateurs à annuler une opération d’envoi, appelez [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) pour implémenter cette fonctionnalité. **AbortSubmit** supprime le message de la file d’attente sortante. Les utilisateurs peuvent être autorisés à empêcher l’envoi jusqu’à ce que le message soit remis au système de messagerie sous-jacent. 
  
Si **SubmitMessage** renvoie MAPI_E_CORRUPT_DATA, supposons que les données envoyées sont maintenant perdues. Avant d’essayer d’envoyer une deuxième fois, réécrire le message en appelant [IMAPIProp::SetProps](imapiprop-setprops.md) et [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Affichez une erreur à l’utilisateur si ces appels **IMAPIProp** échouent ou si **SubmitMessage** échoue une deuxième fois. 
  
Après un appel réussi à **SubmitMessage,** libérez toute mémoire allouée à la liste des destinataires et libérez le message et ses pièces jointes. Une fois qu’un message a été envoyé, MAPI n’autorise pas d’autres opérations sur les pointeurs pour ces objets. La seule exception est **d’appeler IUnknown::Release**. Aucun autre appel n’est autorisé, car de nombreux fournisseurs de magasins de messages invalident les identificateurs d’entrée pour les messages qui ont été envoyés.
  

