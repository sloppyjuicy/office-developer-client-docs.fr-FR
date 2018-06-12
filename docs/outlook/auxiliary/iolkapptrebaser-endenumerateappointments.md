---
title: IOlkApptRebaserEndEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc4506c7-7a4f-940d-d0a6-e0fab4561a88
description: Attend pour l'énumération de rendez-vous dans un dossier de calendrier pour terminer et renvoie une liste de rendez-vous à cette nécessité la relocalisation.
ms.openlocfilehash: d7d29a88114d7b3973b8f04e924dc1dd8489a097
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782748"
---
# <a name="iolkapptrebaserendenumerateappointments"></a><span data-ttu-id="6a799-103">IOlkApptRebaser::EndEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="6a799-103">IOlkApptRebaser::EndEnumerateAppointments</span></span>

<span data-ttu-id="6a799-104">Attend pour l'énumération de rendez-vous dans un dossier de calendrier pour terminer et renvoie une liste de rendez-vous à cette nécessité la relocalisation.</span><span class="sxs-lookup"><span data-stu-id="6a799-104">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6a799-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="6a799-105">Quick info</span></span>

<span data-ttu-id="6a799-106">Voir [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="6a799-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndEnumerateAppointments( 
    void *pContext, 
    HRESULT *phResult, 
    MAPIERROR **ppError, 
    SRowSet **ppRows);
```

## <a name="parameters"></a><span data-ttu-id="6a799-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a799-107">Parameters</span></span>

<span data-ttu-id="6a799-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="6a799-108">_pContext_</span></span>
  
> <span data-ttu-id="6a799-p101">[in] Obligatoire. Pointeur vers le contexte obtenu par un appel préalable à [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="6a799-p101">[in] Required. A pointer to the context obtained from a prior call to [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).</span></span>
    
<span data-ttu-id="6a799-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="6a799-111">_phResult_</span></span>
  
> <span data-ttu-id="6a799-p102">[out] Obligatoire. Pointeur vers **HRESULT** pour récupérer les résultats de l'opération d'énumération.</span><span class="sxs-lookup"><span data-stu-id="6a799-p102">[out] Required. A pointer to an **HRESULT** to retrieve the results of the enumeration operation.</span></span> 
    
<span data-ttu-id="6a799-114">_ppError_</span><span class="sxs-lookup"><span data-stu-id="6a799-114">_ppError_</span></span>
  
> <span data-ttu-id="6a799-p103">[out] Facultatif. Pointeur vers un pointeur vers une structure **MAPIERROR** pour extraire des informations d'erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="6a799-p103">[out] Optional. A pointer to a pointer to a **MAPIERROR** structure to retrieve extended error information.</span></span> 
    
<span data-ttu-id="6a799-117">_ppRows_</span><span class="sxs-lookup"><span data-stu-id="6a799-117">_ppRows_</span></span>
  
> <span data-ttu-id="6a799-p104">[out] Obligatoire. Pointeur vers un pointeur vers une structure [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) qui décrit les rendez-vous qui ont besoin de relocalisation. Cette structure sera généralement passée à [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="6a799-p104">[out] Required. A pointer to a pointer to an [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing. This structure will usually be passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="6a799-121">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="6a799-121">Return values</span></span>

<span data-ttu-id="6a799-122">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="6a799-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a799-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a799-123">See also</span></span>

- [<span data-ttu-id="6a799-124">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="6a799-124">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

