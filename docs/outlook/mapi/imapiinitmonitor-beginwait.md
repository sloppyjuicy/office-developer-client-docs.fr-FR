---
title: imapiinitmonitor-beginwait
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIINITMONITOR.BeginWait
api_type:
- COM
ms.assetid: 71f565a9-651c-42b5-9102-91b728b681ae
description: IMAPIInitMonitor::BeginWait »
Last modified: April 27, 2021
ms.openlocfilehash: beda62b375ce39283030409149c7130ffbcfd517
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564238"
---
# <a name="imapiinitmonitorbeginwait"></a>IMAPIInitMonitor::BeginWait
  
**S’applique** à : Outlook 2016 | Outlook 2019
  
Démarrez une attente pour l’initialisation de MAPI ou le nombre spécifié de millisecondes qui s’écoulént. Cette commande renvoie une interface IMAPIWaitResult qui doit avoir **appelé IMAPIWaitResult::End** pour lancer l’attente. Cela permet à l’appelant de contrôler quel thread est bloqué pendant que nous sommes en attente.

```cpp
HRESULT IMAPIInitMonitor::BeginWait(DWORD timeout, IMAPIWaitResult** ppResult)
```

## <a name="parameters"></a>Paramètres
_timeout_
>[in] Nombre de millisecondes d’attente pour l’initialisation de MAPI, qui peut être définie sur INFINITE pour attendre indéfiniment que l’initialisation se produise.

_ppResult_
>[out] Pointeur pour recevoir l’interface d’attente nouvellement créé.

## <a name="return-value"></a>Valeur renvoyée
S_OK
>Une opération d’attente a été correctement démarrée.

E_OUTOFMEMORY
>Il n’y avait pas assez de mémoire pour créer un objet.

## <a name="remarks"></a>Remarques
Cette API a fourni à l’appelant une interface (thread-safe) qui peut être utilisée pour lancer une attente de blocage pour l’initialisation de MAPI. Cela permet au consommateur de dérialer la meilleure attente pour attendre son application. Le comportement d’appel de IMAPIWaitResult::End est identique à celui d’IMAPIInitMonitor::Wait.

## <a name="see-also"></a>Voir aussi

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
