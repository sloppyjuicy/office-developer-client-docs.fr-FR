---
title: imapiinitmonitor-beginwait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.BeginWait
api_type:
- COM
ms.assetid: 71f565a9-651c-42b5-9102-91b728b681ae
description: IMAPIInitMonitor::BeginWait »
Last modified: April 26, 2021
ms.openlocfilehash: 43a88507cbfc23b3b842f51e69eb4bd791bcfda8
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062017"
---
# <a name="imapiinitmonitorbeginwait"></a><span data-ttu-id="76aa2-103">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="76aa2-103">IMAPIInitMonitor::BeginWait</span></span>
  
<span data-ttu-id="76aa2-104">**S’applique** à : Outlook 2016 | 2019</span><span class="sxs-lookup"><span data-stu-id="76aa2-104">**Applies to**: Outlook 2016 | 2019</span></span>
  
<span data-ttu-id="76aa2-105">Démarrez une attente pour l’initialisation de MAPI ou le nombre spécifié de millisecondes qui s’écoulént.</span><span class="sxs-lookup"><span data-stu-id="76aa2-105">Start a wait for MAPI initialization or the specified number of milliseconds to elapse.</span></span> <span data-ttu-id="76aa2-106">Cette commande renvoie une interface IMAPIWaitResult qui doit avoir **appelé IMAPIWaitResult::End** pour lancer l’attente.</span><span class="sxs-lookup"><span data-stu-id="76aa2-106">This returns an IMAPIWaitResult interface which should have **IMAPIWaitResult::End** called in order initiate the wait.</span></span> <span data-ttu-id="76aa2-107">Cela permet à l’appelant de contrôler quel thread est bloqué pendant que nous sommes en attente.</span><span class="sxs-lookup"><span data-stu-id="76aa2-107">This allows the caller to control which thread is blocked while we are waiting.</span></span>

```cpp
HRESULT IMAPIInitMonitor::BeginWait(DWORD timeout, IMAPIWaitResult** ppResult)
```

## <a name="parameters"></a><span data-ttu-id="76aa2-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="76aa2-108">Parameters</span></span>
<span data-ttu-id="76aa2-109">_timeout_</span><span class="sxs-lookup"><span data-stu-id="76aa2-109">_timeout_</span></span>
><span data-ttu-id="76aa2-110">[in] Nombre de millisecondes d’attente pour l’initialisation de MAPI, qui peut être définie sur INFINITE pour attendre indéfiniment que l’initialisation se produise.</span><span class="sxs-lookup"><span data-stu-id="76aa2-110">[in] The number of millisecond to wait for MAPI initialization, this can set to INFINITE to wait forever for the initialization to happen.</span></span>

<span data-ttu-id="76aa2-111">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="76aa2-111">_ppResult_</span></span>
><span data-ttu-id="76aa2-112">[out] Pointeur pour recevoir l’interface d’attente nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="76aa2-112">[out] A pointer to recieve the newly create wait interface.</span></span>

## <a name="return-value"></a><span data-ttu-id="76aa2-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="76aa2-113">Return value</span></span>
<span data-ttu-id="76aa2-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="76aa2-114">S_OK</span></span>
><span data-ttu-id="76aa2-115">Une opération d’attente a été correctement démarrée.</span><span class="sxs-lookup"><span data-stu-id="76aa2-115">A wait operation was successfully started.</span></span>

<span data-ttu-id="76aa2-116">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="76aa2-116">E_OUTOFMEMORY</span></span>
><span data-ttu-id="76aa2-117">Il n’y avait pas assez de mémoire pour créer un objet</span><span class="sxs-lookup"><span data-stu-id="76aa2-117">There was not enough memory to create a new object</span></span>

## <a name="remarks"></a><span data-ttu-id="76aa2-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="76aa2-118">Remarks</span></span>
<span data-ttu-id="76aa2-119">Cette API a fourni à l’appelant une interface (thread-safe) qui peut être utilisée pour lancer une attente de blocage pour l’initialisation de MAPI.</span><span class="sxs-lookup"><span data-stu-id="76aa2-119">This API provided the caller with an interface (which is thread-safe) which can be used initiate a blocking wait for MAPI initialization.</span></span> <span data-ttu-id="76aa2-120">Cela permet au consommateur de dérialer la meilleure attente pour attendre son application.</span><span class="sxs-lookup"><span data-stu-id="76aa2-120">This allows the consumer to deterime the best wait to wait for thier application.</span></span>   <span data-ttu-id="76aa2-121">Le comportement d’appel de IMAPIWaitResult::End est identique à celui d’IMAPIInitMonitor::Wait.</span><span class="sxs-lookup"><span data-stu-id="76aa2-121">The behavior of calling IMAPIWaitResult::End is identical to calling IMAPIInitMonitor::Wait.</span></span>

## <a name="see-also"></a><span data-ttu-id="76aa2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76aa2-122">See also</span></span>

[<span data-ttu-id="76aa2-123">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="76aa2-123">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="76aa2-124">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="76aa2-124">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md)

[<span data-ttu-id="76aa2-125">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="76aa2-125">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md)

[<span data-ttu-id="76aa2-126">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="76aa2-126">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)

[<span data-ttu-id="76aa2-127">IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="76aa2-127">IMAPIWaitResult</span></span>](imapiwaitresultiunknown.md)
