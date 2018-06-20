---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Définit un bloc de données et de disponibilité. Il s’agit d’un élément dans un calendrier représenté par une demande de réunion ou de rendez-vous.
ms.openlocfilehash: 93418e3777e9d9f0a016822ea5897b8fccc37ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782551"
---
# <a name="fbblock1"></a><span data-ttu-id="28d84-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="28d84-104">FBBlock_1</span></span>

<span data-ttu-id="28d84-105">Définit un bloc de données et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="28d84-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="28d84-106">Il s’agit d’un élément dans un calendrier représenté par une demande de réunion ou de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="28d84-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="28d84-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="28d84-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="28d84-108">Membres</span><span class="sxs-lookup"><span data-stu-id="28d84-108">Members</span></span>

<span data-ttu-id="28d84-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="28d84-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="28d84-110">L’heure de début pour le bloc, exprimée en heure relative.</span><span class="sxs-lookup"><span data-stu-id="28d84-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="28d84-111">Pour plus d’informations, voir [heure relative utilisés pour accéder aux données et de disponibilité](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="28d84-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="28d84-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="28d84-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="28d84-113">L’heure de fin pour le bloc, exprimée en heure relative.</span><span class="sxs-lookup"><span data-stu-id="28d84-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="28d84-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="28d84-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="28d84-115">L’état de disponibilité pour ce bloc, qui indique si l’utilisateur est absent du bureau, occupé (e), provisoire ou gratuite, au cours de la période de temps entre _m_tmStart_ et _m_tmEnd_.</span><span class="sxs-lookup"><span data-stu-id="28d84-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28d84-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28d84-116">See also</span></span>

- [<span data-ttu-id="28d84-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="28d84-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="28d84-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="28d84-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="28d84-119">Utiliser l’heure relative pour accéder aux données et de disponibilité</span><span class="sxs-lookup"><span data-stu-id="28d84-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

