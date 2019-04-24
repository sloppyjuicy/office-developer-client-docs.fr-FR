---
title: À propos de l'indexation du magasin basé sur les notifications
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322133"
---
# <a name="about-notification-based-store-indexing"></a>À propos de l'indexation du magasin basé sur les notifications

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur de banque MAPI peut spécifier si le gestionnaire de protocole MAPI analyse et indexe les messages dans la Banque, ou si le magasin envoie des notifications à l'indexeur lorsque des messages sont indexés. Ce dernier est appelé indexation basée sur les notifications, et un magasin qui prend en charge l'indexation basée sur les notifications est appelé magasin de diffuseurs.
  
Un fournisseur de banque qui prend en charge l'indexation basée sur la notification définit l'indicateur **STORE_PUSHER_OK** dans la propriété **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** . Le gestionnaire de protocole MAPI ou un client peut obtenir la propriété **PR_STORE_SUPPORT_MASK** pour déterminer les caractéristiques de la Banque. 
  
Chaque fois qu'une pièce jointe, un dossier ou un message doit être indexé, le fournisseur de banque d'adresses génère une URL (Uniform Resource Locator) MAPI qui identifie l'objet à indexer et l'envoie à l'indexeur. Cette URL MAPI est codée en Unicode et doit identifier de manière unique l'objet dans le gestionnaire de protocole MAPI. Pour plus d'informations sur les URL MAPI, reportez-vous à la rubrique [à propos des URL MAPI pour l'indexation basée sur les notifications](about-mapi-urls-for-notification-based-indexing.md).
  
Étant donné qu'un indexeur ne peut pas toujours indexer tous les éléments avant qu'un arrêt ait lieu dans un magasin de pousseurs, le magasin de Push doit conserver ce qui doit être poussé. Lorsqu'un fournisseur de banque d'informations envoie une notification sur un objet qui doit être indexé, il spécifie le type de notification **fnevIndexing** dans le membre **ulEventType** de la structure de **[notification](notification.md)** . Le membre **info** de la structure **NOTIFICATION** contient une structure **[EXTENDED_NOTIFICATION](extended_notification.md)**. Le fournisseur Store identifie le processus dans la propriété **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** . Il identifie également le processus dans la structure [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) et transmet ces informations dans le cadre du membre **pbEventParameters** de la structure **EXTENDED_NOTIFICATION** . Si le processus est arrêté ou se bloque, le gestionnaire de protocole MAPI pourra immédiatement le détecter et arrêter l'indexation du magasin de transmission de contenu. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de magasin](about-the-store-api.md)
  
[Constantes MAPI](mapi-constants.md)

