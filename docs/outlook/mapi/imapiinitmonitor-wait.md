---
title: imapiinitmonitor-wait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.Wait
api_type:
- COM
ms.assetid: ed566cae-35a2-4716-817b-54d1ba6825c6
description: IMAPIAMonitor::Wait
Last modified: April 26, 2021
ms.openlocfilehash: ee46a2744e67804c9dfdac8d7512db1d7b07f8ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062010"
---
# <a name="imapiinitmonitorwait"></a>IMAPIInitMonitor::Wait
  
**S’applique** à : Outlook 2013 | Outlook 2016 | 2019
  
Lance un appel BLOCKING sur ce thread, qui retourne soit lorsque le nombre de millisecondes spécifié est écoulé, soit que MAPI a été initialisé. INFINITE peut être utilisé pour une attente infinie.

```cpp
HRESULT IMAPIInitMonitor::Wait(DWORD timeout)
```

## <a name="parameters"></a>Parameters
_timeout_
> [in] Le nombre de millisecondes à attendre pour l’initialisation de MAPI, vous pouvez transmettre INFINITE (0xFFFFFFFF) pour attendre indéfiniment.

## <a name="return-value"></a>Valeur renvoyée

S_OK
> MAPI a été initialisé avec succès.

HRESULT_FROM_WIN32(ERROR_TIMEOUT)
> En cas de délai non infini, cela indique que MAPI n’a pas été initialisé pendant cette période.

## <a name="remarks"></a>Remarques
  
## <a name="see-also"></a>Voir aussi

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
