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
# <a name="imapiinitmonitorwait"></a><span data-ttu-id="438c1-103">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="438c1-103">IMAPIInitMonitor::Wait</span></span>
  
<span data-ttu-id="438c1-104">**S’applique** à : Outlook 2013 | Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="438c1-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="438c1-105">Lance un appel BLOCKING sur ce thread, qui retourne soit lorsque le nombre de millisecondes spécifié est écoulé, soit que MAPI a été initialisé.</span><span class="sxs-lookup"><span data-stu-id="438c1-105">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span> <span data-ttu-id="438c1-106">INFINITE peut être utilisé pour une attente infinie.</span><span class="sxs-lookup"><span data-stu-id="438c1-106">INFINITE can be used to for an infinite wait.</span></span>

```cpp
HRESULT IMAPIInitMonitor::Wait(DWORD timeout)
```

## <a name="parameters"></a><span data-ttu-id="438c1-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="438c1-107">Parameters</span></span>
<span data-ttu-id="438c1-108">_timeout_</span><span class="sxs-lookup"><span data-stu-id="438c1-108">_timeout_</span></span>
> <span data-ttu-id="438c1-109">[in] Le nombre de millisecondes à attendre pour l’initialisation de MAPI, vous pouvez transmettre INFINITE (0xFFFFFFFF) pour attendre indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="438c1-109">[in] The number of milliseconds to wait for MAPI to be initialized, you can pass INFINITE (0xFFFFFFFF) to wait forever.</span></span>

## <a name="return-value"></a><span data-ttu-id="438c1-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="438c1-110">Return value</span></span>

<span data-ttu-id="438c1-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="438c1-111">S_OK</span></span>
> <span data-ttu-id="438c1-112">MAPI a été initialisé avec succès.</span><span class="sxs-lookup"><span data-stu-id="438c1-112">MAPI has been initialized successfully.</span></span>

<span data-ttu-id="438c1-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="438c1-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span></span>
> <span data-ttu-id="438c1-114">En cas de délai non infini, cela indique que MAPI n’a pas été initialisé pendant cette période.</span><span class="sxs-lookup"><span data-stu-id="438c1-114">When given a non-infinite timeout this indicates MAPI was not initialized during that period.</span></span>

## <a name="remarks"></a><span data-ttu-id="438c1-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="438c1-115">Remarks</span></span>
  
## <a name="see-also"></a><span data-ttu-id="438c1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="438c1-116">See also</span></span>

[<span data-ttu-id="438c1-117">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="438c1-117">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="438c1-118">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="438c1-118">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="438c1-119">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="438c1-119">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="438c1-120">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="438c1-120">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="438c1-121">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="438c1-121">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
