---
title: IMAPIWaitResult::End
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIWaitResult.End
api_type:
- COM
ms.assetid: 7463c9e8-d065-4cc3-ac01-d428b57bbc88
description: IMAPIWaitResult::End
Last modified: April 27, 2021
ms.openlocfilehash: 7cc5e122f71399232c07d94a13598b0c9a6fed31
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630557"
---
# <a name="imapiwaitresultend"></a>IMAPIWaitResult::End
  
**S’applique** à : Outlook 2013 | Outlook 2016 | Outlook 2019

Lance un appel BLOCKING sur ce thread, qui retourne soit lorsque le nombre de millisecondes spécifié est écoulé, soit que MAPI a été initialisé. INFINITE peut être utilisé pour une attente infinie.

```cpp
HRESULT IMAPIWaitResult::End(DWORD timeout)
```

## <a name="parameters"></a>Paramètres

_timeout_
> [in] Le nombre de millisecondes à attendre pour l’initialisation de MAPI, vous pouvez transmettre INFINITE (0xFFFFFFFF) pour attendre indéfiniment.

## <a name="return-value"></a>Valeur renvoyée

S_OK
> MAPI a été initialisé avec succès

HRESULT_FROM_WIN32(ERROR_TIMEOUT)
> En cas de délai non infini, cela indique que MAPI n’a pas été initialisé pendant cette période.

## <a name="remarks"></a>Remarques
Cette API se comporte exactement comme [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).
  
## <a name="see-also"></a>Voir aussi

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
