---
title: IMAPIWaitResult::End
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWaitResult.End
api_type:
- COM
ms.assetid: 7463c9e8-d065-4cc3-ac01-d428b57bbc88
description: IMAPIWaitResult::End
Last modified: April 26, 2021
ms.openlocfilehash: 3432bf3b71fa7e15cb4621d461a8d4bbe962f1ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062031"
---
# <a name="imapiwaitresultend"></a><span data-ttu-id="6e0fa-103">IMAPIWaitResult::End</span><span class="sxs-lookup"><span data-stu-id="6e0fa-103">IMAPIWaitResult::End</span></span>
  
<span data-ttu-id="6e0fa-104">**S’applique** à : Outlook 2013 | Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="6e0fa-104">**Applies to**: Outlook 2013 | Outlook 2016 | 2019</span></span>

<span data-ttu-id="6e0fa-105">Lance un appel BLOCKING sur ce thread, qui retourne soit lorsque le nombre de millisecondes spécifié est écoulé, soit que MAPI a été initialisé.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-105">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span> <span data-ttu-id="6e0fa-106">INFINITE peut être utilisé pour une attente infinie.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-106">INFINITE can be used to for an infinite wait.</span></span>

```cpp
HRESULT IMAPIWaitResult::End(DWORD timeout)
```

## <a name="parameters"></a><span data-ttu-id="6e0fa-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="6e0fa-107">Parameters</span></span>

<span data-ttu-id="6e0fa-108">_timeout_</span><span class="sxs-lookup"><span data-stu-id="6e0fa-108">_timeout_</span></span>
> <span data-ttu-id="6e0fa-109">[in] Le nombre de millisecondes à attendre pour l’initialisation de MAPI, vous pouvez transmettre INFINITE (0xFFFFFFFF) pour attendre indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-109">[in] The number of millisecond to wait for MAPI to be initialized, you can pass INFINITE (0xFFFFFFFF) to wait forever.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e0fa-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6e0fa-110">Return value</span></span>

<span data-ttu-id="6e0fa-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e0fa-111">S_OK</span></span>
> <span data-ttu-id="6e0fa-112">MAPI a été initialisé avec succès</span><span class="sxs-lookup"><span data-stu-id="6e0fa-112">MAPI has been initialized successfully</span></span>

<span data-ttu-id="6e0fa-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="6e0fa-113">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span></span>
> <span data-ttu-id="6e0fa-114">En cas de délai non infini, cela indique que MAPI n’a pas été initialisé pendant cette période.</span><span class="sxs-lookup"><span data-stu-id="6e0fa-114">When given a non-infinite timeout this indicates MAPI was not initialized during that period.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e0fa-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e0fa-115">Remarks</span></span>
<span data-ttu-id="6e0fa-116">Cette API se comporte exactement comme [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).</span><span class="sxs-lookup"><span data-stu-id="6e0fa-116">This API behaves exactly the same as [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e0fa-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e0fa-117">See also</span></span>

[<span data-ttu-id="6e0fa-118">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="6e0fa-118">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="6e0fa-119">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="6e0fa-119">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="6e0fa-120">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="6e0fa-120">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="6e0fa-121">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="6e0fa-121">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
