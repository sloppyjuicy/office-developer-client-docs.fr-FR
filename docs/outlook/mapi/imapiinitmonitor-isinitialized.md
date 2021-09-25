---
title: imapiinitmonitor-isinitialized
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIINITMONITOR.IsInitialized
api_type:
- COM
ms.assetid: 1af0bf93-6bcb-4235-ac30-0d00245ec636
description: IMAPIInitMonitor::IsInitialized
Last modified: April 27, 2021
ms.openlocfilehash: 922ce2f978b5ecfb6c2b34873f7b750b6022035f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564245"
---
# <a name="imapiinitmonitorisinitialized"></a>IMAPIInitMonitor::IsInitialized
  
**S’applique** à : Outlook 2013 | Outlook 2016 | Outlook 2019
  
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
