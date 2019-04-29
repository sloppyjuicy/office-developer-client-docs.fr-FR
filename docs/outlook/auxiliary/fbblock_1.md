---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Définit un bloc de données de disponibilité. Il s'agit d'un élément d'un calendrier représenté par une demande de rendez-vous ou de réunion.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413198"
---
# <a name="fbblock1"></a><span data-ttu-id="38728-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="38728-104">FBBlock_1</span></span>

<span data-ttu-id="38728-105">Définit un bloc de données de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="38728-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="38728-106">Il s'agit d'un élément d'un calendrier représenté par une demande de rendez-vous ou de réunion.</span><span class="sxs-lookup"><span data-stu-id="38728-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="38728-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="38728-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="38728-108">Membres</span><span class="sxs-lookup"><span data-stu-id="38728-108">Members</span></span>

<span data-ttu-id="38728-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="38728-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="38728-110">Heure de début du bloc, exprimée en heure relative.</span><span class="sxs-lookup"><span data-stu-id="38728-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="38728-111">Pour plus d'informations, consultez la rubrique [utilisation de l'heure relative pour accéder aux données de](how-to-use-relative-time-to-access-free-busy-data.md)disponibilité.</span><span class="sxs-lookup"><span data-stu-id="38728-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="38728-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="38728-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="38728-113">Heure de fin du bloc, exprimée en heure relative.</span><span class="sxs-lookup"><span data-stu-id="38728-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="38728-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="38728-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="38728-115">État de disponibilité de ce bloc, indiquant si l'utilisateur est absent (e) du bureau, occupé, provisoire ou libre, pendant la période comprise entre _m_tmStart_ et _m_tmEnd_.</span><span class="sxs-lookup"><span data-stu-id="38728-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38728-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38728-116">See also</span></span>

- [<span data-ttu-id="38728-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="38728-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="38728-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="38728-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="38728-119">Utiliser l’heure relative pour accéder aux données de disponibilité</span><span class="sxs-lookup"><span data-stu-id="38728-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

