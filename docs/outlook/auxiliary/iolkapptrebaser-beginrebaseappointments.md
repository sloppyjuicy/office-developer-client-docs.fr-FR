---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: Commence une tâche pour la relocalisation de rendez-vous donné une liste de rendez-vous, généralement obtenu à partir de IOlkApptRebaser::EndEnumerateAppointments.
ms.openlocfilehash: f0f2377f30de7688aaa4196e3a046c664c2128aa
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396091"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a><span data-ttu-id="2b6d0-103">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="2b6d0-103">IOlkApptRebaser::BeginRebaseAppointments</span></span>

<span data-ttu-id="2b6d0-104">Commence une tâche pour la relocalisation de rendez-vous donné une liste de rendez-vous, généralement obtenu à partir de [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="2b6d0-104">Begins a task for appointment rebasing given a list of appointments, usually obtained from [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2b6d0-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="2b6d0-105">Quick info</span></span>

<span data-ttu-id="2b6d0-106">Voir [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="2b6d0-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="2b6d0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b6d0-107">Parameters</span></span>

<span data-ttu-id="2b6d0-108">_pRows_</span><span class="sxs-lookup"><span data-stu-id="2b6d0-108">_pRows_</span></span>
  
> <span data-ttu-id="2b6d0-p101">[in] Obligatoire. Pointeur vers une structure [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) qui décrit les rendez-vous qui ont besoin de relocalisation. Cette structure est généralement obtenue à partir d'un appel antérieur à [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="2b6d0-p101">[in] Required. A pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure is usually obtained from a prior call to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
<span data-ttu-id="2b6d0-112">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="2b6d0-112">_pfnProgress_</span></span>
  
> <span data-ttu-id="2b6d0-p102">[in] Facultatif. Pointeur vers une fonction de la progression de tâche rebase pour recevoir les cours. **PFNREBASETASKPROGRESS** est défini dans tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="2b6d0-p102">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="2b6d0-116">_pfnComplete_</span><span class="sxs-lookup"><span data-stu-id="2b6d0-116">_pfnComplete_</span></span>
  
> <span data-ttu-id="2b6d0-p103">[out] Facultatif. Un pointeur vers une fonction de saisie semi-automatique de tâche rebase pour recevoir une notification d'achèvement rebase. **PFNREBASETASKCOMPLETE** est défini dans tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="2b6d0-p103">[out] Optional. A pointer to a rebase task completion function to receive notification of rebase completion. **PFNREBASETASKCOMPLETE** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="2b6d0-120">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="2b6d0-120">_ppContext_</span></span>
  
> <span data-ttu-id="2b6d0-p104">[out] Obligatoire. Pointeur vers un pointeur vers le contexte retourné. Ce contexte sera généralement passé à [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="2b6d0-p104">[out] Required. A pointer to a pointer to the returned context. This context will usually be passed to [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="2b6d0-124">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="2b6d0-124">Return values</span></span>

<span data-ttu-id="2b6d0-125">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="2b6d0-125">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b6d0-126">Note</span><span class="sxs-lookup"><span data-stu-id="2b6d0-126">Remarks</span></span>

<span data-ttu-id="2b6d0-127">Cette tâche s'exécute sur un nouveau thread.</span><span class="sxs-lookup"><span data-stu-id="2b6d0-127">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b6d0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b6d0-128">See also</span></span>

- [<span data-ttu-id="2b6d0-129">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="2b6d0-129">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

