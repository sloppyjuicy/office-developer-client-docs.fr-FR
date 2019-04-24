---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Attend des rendez-vous pour terminer la relocalisation et récupère les résultats.
ms.openlocfilehash: a6e62cff9efea1fc7079d04bc9b032b5637f8847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321888"
---
# <a name="iolkapptrebaserendrebaseappointments"></a><span data-ttu-id="f63dc-103">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="f63dc-103">IOlkApptRebaser::EndRebaseAppointments</span></span>

<span data-ttu-id="f63dc-104">Attend des rendez-vous pour terminer la relocalisation et récupère les résultats.</span><span class="sxs-lookup"><span data-stu-id="f63dc-104">Waits for appointment rebasing to complete and retrieves the results.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f63dc-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="f63dc-105">Quick info</span></span>

<span data-ttu-id="f63dc-106">Voir [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="f63dc-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a><span data-ttu-id="f63dc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f63dc-107">Parameters</span></span>

<span data-ttu-id="f63dc-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="f63dc-108">_pContext_</span></span>
  
> <span data-ttu-id="f63dc-p101">[in] Obligatoire. Pointeur vers le contexte obtenu par un appel à [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="f63dc-p101">[in] Required. A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="f63dc-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="f63dc-111">_phResult_</span></span>
  
> <span data-ttu-id="f63dc-p102">[out] Obligatoire. Pointeur vers **HRESULT** pour extraire le résultat de l'opération de relocalisation.</span><span class="sxs-lookup"><span data-stu-id="f63dc-p102">[out] Required. A pointer to an **HRESULT** to retrieve the result of the rebasing operation.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f63dc-114">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="f63dc-114">Return values</span></span>

<span data-ttu-id="f63dc-115">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="f63dc-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f63dc-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f63dc-116">See also</span></span>

- [<span data-ttu-id="f63dc-117">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="f63dc-117">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

