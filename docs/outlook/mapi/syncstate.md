---
title: SYNCSTATE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 63c47e94-f603-aef9-afed-e3819bd79408
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 080556a7ed4530bb96db20fd96d9dda86672a720
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787339"
---
# <a name="syncstate"></a>SYNCSTATE

**S’applique à**: Outlook 
  
Cette structure définit les États pour l’ordinateur d’état de réplication.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef enum { 
    LR_SYNC_IDLE = 0, 
    LR_SYNC, 
    LR_SYNC_UPLOAD_HIERARCHY, 
    LR_SYNC_UPLOAD_FOLDER, 
    LR_SYNC_CONTENTS, 
    LR_SYNC_UPLOAD_TABLE, 
    LR_SYNC_UPLOAD_MESSAGE, 
    LR_SYNC_UPLOAD_MESSAGE_READ = 8, 
    LR_SYNC_UPLOAD_MESSAGE_DEL, 
    LR_SYNC_DOWNLOAD_HIERARCHY, 
    LR_SYNC_DOWNLOAD_TABLE, 
    LR_SYNC_DOWNLOAD_HEADER = 17 
} SYNCSTATE; 

```

## <a name="see-also"></a>Voir aussi

- [À propos de l’API de réplication](about-the-replication-api.md)
- [Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)

