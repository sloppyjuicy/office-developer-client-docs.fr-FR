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
# <a name="imapiinitmonitorisinitialized"></a><span data-ttu-id="cf85a-103">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="cf85a-103">IMAPIInitMonitor::IsInitialized</span></span>
  
<span data-ttu-id="cf85a-104">**S'applique** à : Outlook 2013 | Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="cf85a-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="cf85a-105">Interroge MAPI pour déterminer s'il est actuellement initialisé dans le processus d'appel.</span><span class="sxs-lookup"><span data-stu-id="cf85a-105">Queries MAPI to determine if it currently initialized in the calling process.</span></span>

```cpp
BOOL IMAPIInitMonitor::IsInitialized()  
```

## <a name="parameters"></a><span data-ttu-id="cf85a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf85a-106">Parameters</span></span>
<span data-ttu-id="cf85a-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="cf85a-107">None</span></span>

## <a name="return-value"></a><span data-ttu-id="cf85a-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cf85a-108">Return value</span></span>
<span data-ttu-id="cf85a-109">Un bool indiquant l'état actuel de l'initialisation MAPI, une valeur true signifie que MAPI a été initialisé et est disponible pour utilisation, tandis qu'une valeur false signifie que MAPI n'est actuellement pas initialisé et n'est pas prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="cf85a-109">A BOOL indicating the current state of MAPI initialization, a value of TRUE means MAPI has been initialized and is available for use, while a value of FALSE means MAPI is currenty uninitialized and is not ready be consumed.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf85a-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf85a-110">Remarks</span></span>
<span data-ttu-id="cf85a-111">Cela peut être utilisé pour déterminer si MAPI est prêt à être utilisé, par exemple, si votre application souhaite faire quelque chose uniquement si MAPI a déjà été initialisé, cela peut être une vérification utile dans une tâche en arrière-plan pour empêcher le coût de rotation de MAPI pour le travail facultatif.</span><span class="sxs-lookup"><span data-stu-id="cf85a-111">This can be used to determine if MAPI is ready to be used, for example, if your application wanted to do something only if MAPI has already be initialized, this could be a useful check in a background task to prevent the cost of spinning up MAPI for optional work.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf85a-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf85a-112">See also</span></span>

[<span data-ttu-id="cf85a-113">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="cf85a-113">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md)

[<span data-ttu-id="cf85a-114">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="cf85a-114">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)
