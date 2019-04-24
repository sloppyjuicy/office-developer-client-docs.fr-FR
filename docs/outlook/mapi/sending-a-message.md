---
title: Envoi d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339745"
---
# <a name="sending-a-message"></a>Envoi d’un message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque vous êtes prêt à envoyer un message, appelez sa méthode [IMessage:: SubmitMessage](imessage-submitmessage.md) . **SubmitMessage** place le message dans la file d'attente sortante et définit l'indicateur MSGFLAG_SUBMIT dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message.
  
Le fournisseur de banque de messages, s'il est étroitement couplé à un fournisseur de transport, transmet directement le message au transport qui le remet au système de messagerie. Si elle n'est pas étroitement couplée, le fournisseur de banque de messages informe le spouleur MAPI que la file d'attente sortante a été modifiée et que le spouleur MAPI transfère le message à un fournisseur de transport approprié.
  
Si vous permettez aux utilisateurs d'annuler une opération d'envoi, appelez [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) pour implémenter cette fonctionnalité. **AbortSubmit** supprime le message de la file d'attente sortante. Les utilisateurs peuvent être autorisés à arrêter une émission jusqu'à ce que le message soit donné au système de messagerie sous-jacent. 
  
Si **SubmitMessage** renvoie MAPI_E_CORRUPT_DATA, partez du principe que les données envoyées sont maintenant perdues. Avant d'essayer d'envoyer une deuxième fois, ré-écrivez le message en appelant [IMAPIProp:: SetProps](imapiprop-setprops.md) et [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). Afficher une erreur à l'utilisateur si ces appels **IMAPIProp** échouent ou si **SubmitMessage** échoue une deuxième fois. 
  
Après un appel réussi vers **SubmitMessage**, libérez de la mémoire allouée à la liste des destinataires, puis libérez le message et ses pièces jointes. Une fois qu'un message a été envoyé, MAPI n'autorise pas d'autres opérations sur les pointeurs pour ces objets. La seule exception est l'appel de **IUnknown:: Release**. Aucun autre appel n'est autorisé car de nombreux fournisseurs de banques de messages invalident des identificateurs d'entrée pour les messages qui ont été envoyés.
  

