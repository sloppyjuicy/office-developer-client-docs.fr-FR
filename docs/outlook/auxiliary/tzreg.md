---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Définit le démarrage de l’heure, quand le retour à l’heure standard se produit et le nombre d’heures du passage de MAJ est.
ms.openlocfilehash: 85812ab053d77c07f9360b6bf3a1faaf72cae573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782840"
---
# <a name="tzreg"></a><span data-ttu-id="59d38-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="59d38-103">TZREG</span></span>

<span data-ttu-id="59d38-104">Définit le démarrage de l’heure, quand le retour à l’heure standard se produit et le nombre d’heures du passage de MAJ est.</span><span class="sxs-lookup"><span data-stu-id="59d38-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="59d38-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="59d38-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="59d38-106">Membres</span><span class="sxs-lookup"><span data-stu-id="59d38-106">Members</span></span>

<span data-ttu-id="59d38-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="59d38-107">_lBias_</span></span>
  
> <span data-ttu-id="59d38-108">Décalage de l’heure de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="59d38-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="59d38-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="59d38-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="59d38-110">Décalage de décalage au cours de l’heure standard.</span><span class="sxs-lookup"><span data-stu-id="59d38-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="59d38-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="59d38-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="59d38-112">Décalage de décalage de l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="59d38-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="59d38-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="59d38-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="59d38-114">Le temps de passer à l’heure standard.</span><span class="sxs-lookup"><span data-stu-id="59d38-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="59d38-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="59d38-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="59d38-116">Le temps de passer à l’heure d’été.</span><span class="sxs-lookup"><span data-stu-id="59d38-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="59d38-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="59d38-117">Remarks</span></span>

<span data-ttu-id="59d38-118">Cette structure est similaire à **TIME_ZONE_INFORMATION**.</span><span class="sxs-lookup"><span data-stu-id="59d38-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="59d38-119">Il s’agit de la structure permet de stocker les informations de fuseau horaire pour les réunions périodiques par les clients hérités.</span><span class="sxs-lookup"><span data-stu-id="59d38-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="59d38-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59d38-120">See also</span></span>

- [<span data-ttu-id="59d38-121">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="59d38-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="59d38-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="59d38-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="59d38-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="59d38-123">TZRULE</span></span>](tzrule.md)

