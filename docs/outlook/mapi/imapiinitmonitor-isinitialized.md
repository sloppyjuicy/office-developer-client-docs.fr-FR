---
title: imapiinitmonitor-isinitialized
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.IsInitialized
api_type:
- COM
ms.assetid: 1af0bf93-6bcb-4235-ac30-0d00245ec636
description: IMAPIInitMonitor::IsInitialized
Last modified: April 26, 2021
ms.openlocfilehash: 6870c8fa0de51b626662c58b2c8c300c3a4d806e
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062024"
---
# <a name="imapiinitmonitorisinitialized"></a>IMAPIInitMonitor::IsInitialized
  
**S’applique** à : Outlook 2013 | Outlook 2016 | 2019
  
Interroge MAPI pour déterminer s’il est actuellement initialisé dans le processus d’appel.

```cpp
BOOL IMAPIInitMonitor::IsInitialized()  
```

## <a name="parameters"></a>Paramètres
Aucun

## <a name="return-value"></a>Valeur renvoyée
Une valeur BOOL indiquant l’état actuel de l’initialisation MAPI, une valeur true signifie que MAPI a été initialisé et est disponible pour utilisation, tandis qu’une valeur FALSE signifie que MAPI n’est actuellement pas initialisé et n’est pas prêt à être utilisé.

## <a name="remarks"></a>Remarques
Cela peut être utilisé pour déterminer si MAPI est prêt à être utilisé, par exemple, si votre application souhaite faire quelque chose uniquement si MAPI a déjà été initialisé, cela peut être une vérification utile dans une tâche en arrière-plan pour empêcher le coût de rotation de MAPI pour le travail facultatif.

## <a name="see-also"></a>Voir aussi

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
