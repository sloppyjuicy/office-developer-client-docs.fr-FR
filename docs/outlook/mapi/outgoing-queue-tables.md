---
title: Tables de files d’attente sortantes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c5f136a0d26b7519bc1b7b3d8f448f5f382767ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591253"
---
# <a name="outgoing-queue-tables"></a>Tables de files d’attente sortantes

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une table sortant de la file d’attente contient des informations sur tous les messages sortants pour une banque de messages. Implémentés par les fournisseurs de banque de message sortant tables de file d’attente pour le spouleur MAPI à utiliser. Magasins qui ne prennent pas en charge l’envoi ou la réception de messages ne doit pas mettre ce tableau. 
  
Pour accéder à une table de file d’attente sortante, le spouleur MAPI appelle la méthode [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) . 
  
Il est nécessaire que les messages prétraités et soumises au fournisseur de transport dans le même ordre qu’ils ont été envoyés par l’application cliente. Le spouleur MAPI est conçu pour accepter les messages de la banque de messages dans l’ordre croissant de l’heure de soumission. En raison de cette exigence, il peut être quelque temps avant que certains messages s’affichent dans le tableau sortant de la file d’attente. 
  
Banques de messages doivent soit autoriser le tri de la table de file d’attente sortante afin que le spouleur MAPI permettre trier les messages par heure de soumission ou l’ordre de tri par défaut doit être par ordre croissant heure de soumission. 
  
Le tableau sortant de la file d’attente doit envoyer des notifications lorsque le contenu de la file d’attente est modifié.
  
Les propriétés suivantes constituent la colonne requise définie dans les tableaux de file d’attente sortant :
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Pour plus d’informations sur l’utilisation de la table sortant de la file d’attente, consultez [Envoi de Messages par les fournisseurs de banque de Message à l’aide](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

