---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Commence une tâche pour l'énumération de rendez-vous dans un dossier de calendrier pour rechercher les rendez-vous qui ont besoin de relocalisation.
ms.openlocfilehash: cc89b3510f09bb98fd6720cb6d5ab3edeb13eac8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407269"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a><span data-ttu-id="0ca1f-103">IOlkApptRebaser::BeginEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="0ca1f-103">IOlkApptRebaser::BeginEnumerateAppointments</span></span>

<span data-ttu-id="0ca1f-104">Commence une tâche pour l'énumération de rendez-vous dans un dossier de calendrier pour rechercher les rendez-vous qui ont besoin de relocalisation.</span><span class="sxs-lookup"><span data-stu-id="0ca1f-104">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0ca1f-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="0ca1f-105">Quick info</span></span>

<span data-ttu-id="0ca1f-106">Voir [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="0ca1f-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="0ca1f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ca1f-107">Parameters</span></span>

<span data-ttu-id="0ca1f-108">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="0ca1f-108">_pfnProgress_</span></span>
  
> <span data-ttu-id="0ca1f-p101">[in] Facultatif. Pointeur vers une fonction de la progression de tâche rebase pour recevoir les cours. **PFNREBASETASKPROGRESS** est défini dans tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="0ca1f-p101">[in] Optional. A pointer to a rebase task progress function to receive progress. **PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="0ca1f-112">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="0ca1f-112">_ppContext_</span></span>
  
> <span data-ttu-id="0ca1f-p102">[out] Obligatoire. Pointeur vers un pointeur vers le contexte retourné. Ce contexte est passé à [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="0ca1f-p102">[out] Required. A pointer to a pointer to the returned context. This context will be passed to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="0ca1f-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0ca1f-116">Return values</span></span>

<span data-ttu-id="0ca1f-117">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="0ca1f-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ca1f-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="0ca1f-118">Remarks</span></span>

<span data-ttu-id="0ca1f-119">Cette tâche s'exécute sur un nouveau thread.</span><span class="sxs-lookup"><span data-stu-id="0ca1f-119">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ca1f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ca1f-120">See also</span></span>

- [<span data-ttu-id="0ca1f-121">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="0ca1f-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

