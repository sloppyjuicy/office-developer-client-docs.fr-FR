---
title: À propos Notification-Based'indexation du Store
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409173"
---
# <a name="about-notification-based-store-indexing"></a>À propos Notification-Based'indexation du Store

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur de magasin MAPI peut spécifier si le fournisseur de protocole MAPI analyse et indexe les messages dans la boutique, ou si la boutique envoie des notifications à l’indexeur lorsqu’il existe des messages à indexer. Ce dernier est connu sous le nom d’indexation basée sur les notifications et un magasin qui prend en charge l’indexation basée sur les notifications est un magasin de push.
  
Un fournisseur de magasins qui prend en charge l’indexation basée sur les notifications définit **l’STORE_PUSHER_OK** dans la **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** de données. Le handler de protocole MAPI ou un client peut obtenir la propriété **PR_STORE_SUPPORT_MASK** pour déterminer les caractéristiques du magasin. 
  
Chaque fois qu’une pièce jointe, un dossier ou un message doit être indexé, le fournisseur de magasins génère une URL (Uniform Resource Locator) MAPI identifiant l’objet à indexer et l’envoie à l’indexeur. Cette URL MAPI est codée en Unicode et doit identifier de manière unique l’objet dans le handler de protocole MAPI. Pour plus d’informations sur les URL MAPI, voir À propos des URL MAPI pour [lNotification-Based indexation.](about-mapi-urls-for-notification-based-indexing.md)
  
Étant donné qu’un indexeur ne peut pas toujours indexer tous les détails avant qu’un arrêt ne se produise dans un magasin de pusher, celui-ci doit conserver ce qui doit être poussée. Lorsqu’un fournisseur de magasin envoie une notification sur un objet qui doit être indexé, il spécifie le type de notification **fnevIndexing** dans le membre **ulEventType** de la structure **[NOTIFICATION.](notification.md)** Le membre **info** de la structure **NOTIFICATION** contient une structure **[EXTENDED_NOTIFICATION](extended_notification.md)**. Le fournisseur de magasin identifie le processus dans la **[propriété PR_SEARCH_OWNER_ID.](pidtagsearchownerid-canonical-property.md)** Il identifie également le processus dans la structure [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) et transmet ces informations dans le cadre du membre **pbEventParameters** de la structure **EXTENDED_NOTIFICATION.** Si le processus est arrêté ou se ferme, le handler de protocole MAPI sera en mesure de détecter cela immédiatement et d’arrêter l’indexation du magasin de pusher. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de magasin](about-the-store-api.md)
  
[Constantes MAPI](mapi-constants.md)

