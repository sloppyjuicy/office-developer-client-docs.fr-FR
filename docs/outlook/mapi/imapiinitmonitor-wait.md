---
title: imapiinitmonitor-wait
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIINITMONITOR.Wait
api_type:
- COM
ms.assetid: ed566cae-35a2-4716-817b-54d1ba6825c6
description: IMAPIAMonitor::Wait
Last modified: April 27, 2021
ms.openlocfilehash: 98111b27b09082c6730b42b0f9d10bdd56d5614c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604907"
---
# <a name="imapiinitmonitorwait"></a>IMAPIInitMonitor::Wait
  
**S’applique** à : Outlook 2013 | Outlook 2016 | Outlook 2019
  
Lance un appel BLOCKING sur ce thread, qui retourne soit lorsque le nombre de millisecondes spécifié est écoulé, soit que MAPI a été initialisé. INFINITE peut être utilisé pour une attente infinie.

```cpp
HRESULT IMAPIInitMonitor::Wait(DWORD timeout)
```

## <a name="parameters"></a>Paramètres
_timeout_
> [in] Le nombre de millisecondes à attendre pour l’initialisation de MAPI, vous pouvez transmettre INFINITE (0xFFFFFFFF) pour attendre indéfiniment.

## <a name="return-value"></a>Valeur renvoyée

S_OK
> MAPI a été initialisé avec succès.

HRESULT_FROM_WIN32(ERROR_TIMEOUT)
> En cas de délai non infini, cela indique que MAPI n’a pas été initialisé pendant cette période.

## <a name="see-also"></a>Voir aussi

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
