---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Définit le début de l’heure d’été, le retour à l’heure standard et le nombre d’heures d’été de l’heure d’été.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419365"
---
# <a name="tzreg"></a><span data-ttu-id="7ee10-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="7ee10-103">TZREG</span></span>

<span data-ttu-id="7ee10-104">Définit le début de l’heure d’été, le retour à l’heure standard et le nombre d’heures d’été de l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="7ee10-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7ee10-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7ee10-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="7ee10-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7ee10-106">Members</span></span>

<span data-ttu-id="7ee10-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="7ee10-107">_lBias_</span></span>
  
> <span data-ttu-id="7ee10-108">Décalage par rapport à l’heure de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="7ee10-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="7ee10-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="7ee10-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="7ee10-110">Décalage par rapport à l’décalage au moment de l’heure standard.</span><span class="sxs-lookup"><span data-stu-id="7ee10-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="7ee10-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="7ee10-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="7ee10-112">Décalage par rapport à l’décalage lors de l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="7ee10-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="7ee10-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="7ee10-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="7ee10-114">Heure de passage à l’heure standard.</span><span class="sxs-lookup"><span data-stu-id="7ee10-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="7ee10-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="7ee10-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="7ee10-116">Heure de passage à l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="7ee10-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ee10-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="7ee10-117">Remarks</span></span>

<span data-ttu-id="7ee10-118">Cette structure est similaire à **TIME_ZONE_INFORMATION**.</span><span class="sxs-lookup"><span data-stu-id="7ee10-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="7ee10-119">Il s’agit de la structure utilisée par les clients hérités pour stocker les informations de fuseau horaire pour les réunions périodiques.</span><span class="sxs-lookup"><span data-stu-id="7ee10-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ee10-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ee10-120">See also</span></span>

- [<span data-ttu-id="7ee10-121">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="7ee10-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="7ee10-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="7ee10-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="7ee10-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="7ee10-123">TZRULE</span></span>](tzrule.md)

