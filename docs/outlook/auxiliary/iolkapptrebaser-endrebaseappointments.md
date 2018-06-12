---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Attend des rendez-vous pour terminer la relocalisation et récupère les résultats.
ms.openlocfilehash: fd27021ce05b1d5b95fd258e0ee89b5bd4f2c7db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782746"
---
# <a name="iolkapptrebaserendrebaseappointments"></a><span data-ttu-id="72f96-103">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="72f96-103">IOlkApptRebaser::EndRebaseAppointments</span></span>

<span data-ttu-id="72f96-104">Attend des rendez-vous pour terminer la relocalisation et récupère les résultats.</span><span class="sxs-lookup"><span data-stu-id="72f96-104">Waits for appointment rebasing to complete and retrieves the results.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="72f96-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="72f96-105">Quick info</span></span>

<span data-ttu-id="72f96-106">Voir [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="72f96-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a><span data-ttu-id="72f96-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72f96-107">Parameters</span></span>

<span data-ttu-id="72f96-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="72f96-108">_pContext_</span></span>
  
> <span data-ttu-id="72f96-p101">[in] Obligatoire. Pointeur vers le contexte obtenu par un appel à [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="72f96-p101">[in] Required. A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="72f96-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="72f96-111">_phResult_</span></span>
  
> <span data-ttu-id="72f96-p102">[out] Obligatoire. Pointeur vers **HRESULT** pour extraire le résultat de l'opération de relocalisation.</span><span class="sxs-lookup"><span data-stu-id="72f96-p102">[out] Required. A pointer to an **HRESULT** to retrieve the result of the rebasing operation.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="72f96-114">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="72f96-114">Return values</span></span>

<span data-ttu-id="72f96-115">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="72f96-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72f96-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72f96-116">See also</span></span>

- [<span data-ttu-id="72f96-117">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="72f96-117">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

