---
title: Tables de file d'attente sortantes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348502"
---
# <a name="outgoing-queue-tables"></a>Tables de file d'attente sortantes

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table de file d'attente sortante contient des informations sur tous les messages sortants d'une banque de messages. Les fournisseurs de banque de messages implémentent des tables de file d'attente sortantes que le spouleur MAPI doit utiliser. Les banques qui ne prennent pas en charge l'envoi ou la réception de messages n'ont pas besoin d'implémenter ce tableau. 
  
Pour accéder à une table de file d'attente de messages sortants, le spouleur MAPI appelle la méthode [IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md) . 
  
Il est nécessaire que les messages soient prétraités et envoyés au fournisseur de transport dans l'ordre dans lequel ils ont été envoyés par l'application cliente. Le spouleur MAPI est conçu pour accepter les messages de la Banque de messages dans l'ordre croissant de la durée de dépôt. En raison de cette exigence, un certain délai peut s'écouler avant que certains messages apparaissent dans la table de file d'attente sortante. 
  
Les banques de messages doivent autoriser le tri sur la table de file d'attente sortante afin que le spouleur MAPI puisse trier les messages par heure de dépôt ou que l'ordre de tri par défaut soit défini par ordre croissant. 
  
La table de file d'attente sortante doit envoyer des notifications lorsque le contenu de la file d'attente est modifié.
  
Les propriétés suivantes constituent le jeu de colonnes obligatoire dans les tables de file d'attente sortantes:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Pour plus d'informations sur l'utilisation de la table de file d'attente de messages sortants, consultez la rubrique [envoi de messages à l'aide de fournisseurs de banques de messages](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

