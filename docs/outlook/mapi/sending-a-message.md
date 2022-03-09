---
title: Envoi d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
ms.openlocfilehash: bd140083a9a455892ebbc42651679451277ff9cc
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376545"
---
# <a name="sending-a-message"></a>Envoi d’un message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous êtes prêt à envoyer un message, appelez sa [méthode IMessage::SubmitMessage](imessage-submitmessage.md) . **SubmitMessage** place le message dans la file d’attente sortante et définit l’indicateur MSGFLAG_SUBMIT dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message.
  
Le fournisseur de magasins de messages, s’il est étroitement associé à un fournisseur de transport, remet le message directement au transport qui le remet au système de messagerie. S’il n’est pas étroitement couplé, le fournisseur de magasin de messages informe lepooler MAPI que la file d’attente sortante a changé et que lepooler MAPI transfère le message à un fournisseur de transport approprié.
  
Si vous autorisez les utilisateurs à annuler une opération d’envoi, appelez [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) pour implémenter cette fonctionnalité. **AbortSubmit** supprime le message de la file d’attente sortante. Les utilisateurs peuvent être autorisés à empêcher l’envoi jusqu’à ce que le message soit remis au système de messagerie sous-jacent. 
  
Si **SubmitMessage** renvoie MAPI_E_CORRUPT_DATA, supposons que les données envoyées sont maintenant perdues. Avant d’essayer d’envoyer un deuxième message, réécrire le message en appelant [IMAPIProp::SetProps](imapiprop-setprops.md) et [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Affichez une erreur à l’utilisateur si ces appels **IMAPIProp** échouent ou si **SubmitMessage** échoue une deuxième fois. 
  
Après un appel réussi à **SubmitMessage**, libérez la mémoire allouée à la liste des destinataires et libérez le message et ses pièces jointes. Une fois qu’un message a été envoyé, MAPI n’autorise pas d’autres opérations sur les pointeurs pour ces objets. La seule exception est **d’appeler IUnknown::Release**. Aucun autre appel n’est autorisé, car de nombreux fournisseurs de magasins de messages invalident les identificateurs d’entrée pour les messages qui ont été envoyés.
  

