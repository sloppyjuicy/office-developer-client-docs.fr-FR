---
title: Tables des files d’attente sortantes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: Une table de file d’attente sortante contient des informations sur les messages sortants d’une boutique de messages. Les fournisseurs implémentent des tables de files d’attente sortantes pour lepooler MAPI à utiliser.
ms.openlocfilehash: deb928a7fe080a70bcf280bbc90cdc7abf3b2d2e
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762976"
---
# <a name="outgoing-queue-tables"></a>Tables des files d’attente sortantes

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table de file d’attente sortante contient des informations sur tous les messages sortants d’une boutique de messages. Les fournisseurs de magasins de messages implémentent des tables de files d’attente sortantes pour lepooler MAPI à utiliser. Les magasins qui ne peuvent pas prendre en charge l’envoi ou la réception de messages n’ont pas besoin d’implémenter cette table. 
  
Pour accéder à une table de files d’attente sortantes, lepooler MAPI appelle la méthode [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) . 
  
Il est obligatoire que les messages soient prétraités et envoyés au fournisseur de transport dans le même ordre qu’ils ont été envoyés par l’application cliente. Lepooler MAPI est conçu pour accepter les messages de la boutique de messages dans l’ordre croissant du temps d’envoi. En raison de cette exigence, il peut y avoir un certain délai avant que certains messages apparaissent dans la table des files d’attente sortantes. 
  
Les magasins de messages doivent autoriser le tri dans la table des files d’attente sortantes afin que lepooler MAPI puisse trier les messages par heure d’envoi, ou l’ordre de tri par défaut doit être croissant. 
  
La table des files d’attente sortantes doit envoyer des notifications lorsque le contenu de la file d’attente change.
  
Les propriétés suivantes définissent la colonne requise dans les tables de files d’attente sortantes :
  
|Property |... |
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Pour plus d’informations sur l’utilisation de la table des files d’attente sortantes, voir [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

