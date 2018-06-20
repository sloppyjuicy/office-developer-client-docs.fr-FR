---
title: Indexation de magasin de Notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 338ae3c3c8d8b4037ab0c7b46916e45cf5a8ded2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782847"
---
# <a name="about-notification-based-store-indexing"></a>Indexation de magasin de Notification

  
  
**S’applique à**: Outlook 
  
Un fournisseur de banque MAPI peut spécifier si les analyses de gestionnaire de protocole MAPI et les index des messages dans le magasin, ou si la banque envoie des notifications à l’indexeur lorsqu’il existe des messages à indexer. Ce dernier est connu en tant que l’indexation basée sur une notification, et un objet store qui prend en charge l’indexation basée sur une notification est connu comme un magasin poussoir.
  
Un fournisseur de banque prend en charge les jeux d’indexation de notification l’indicateur **STORE_PUSHER_OK** dans la propriété **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** . Le Gestionnaire de protocole MAPI ou d’un client peut obtenir la propriété **PR_STORE_SUPPORT_MASK** pour déterminer les caractéristiques de la banque. 
  
Chaque fois qu’il existe une pièce jointe, dossier ou un message à indexer, le fournisseur de banque génère un MAPI URL Uniform Resource Locator () qui identifie l’objet à indexer et l’envoie à l’indexeur. Cette URL MAPI est codée en Unicode et doit identifier de manière unique l’objet dans le Gestionnaire de protocole MAPI. Pour plus d’informations sur les URL MAPI, voir [Sur les URL MAPI pour l’indexation basée sur une Notification](about-mapi-urls-for-notification-based-indexing.md).
  
Un indexeur ne peut pas toujours indexer tout avant un arrêt se produit dans une banque poussoir, la banque poussoir doit conserve les éléments qui doivent être appliquées. Lorsqu’un fournisseur de banque envoie une notification relative à un objet qui doit être indexé, elle spécifie le type de notification **fnevIndexing** dans le membre **ulEventType** de la structure de **[NOTIFICATION](notification.md)** . Membre de la structure de **NOTIFICATION** **info** contient une structure **[EXTENDED_NOTIFICATION](extended_notification.md)** . Le fournisseur de banque identifie le processus dans la propriété **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** . Il identifie le processus de la structure [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) et vous transmet ces informations dans le cadre du membre de la structure **EXTENDED_NOTIFICATION** **pbEventParameters** . Si le processus est arrêté ou se bloque, le Gestionnaire de protocole MAPI sera en mesure de détecter et arrêter l’indexation de la banque poussoir immédiatement. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API du magasin](about-the-store-api.md)
  
[Constantes MAPI](mapi-constants.md)

