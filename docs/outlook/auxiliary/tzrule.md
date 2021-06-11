---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Spécifie les informations d’une règle de fuseau horaire concernant le début de l’heure d’été et l’année pendant laquelle cette règle de fuseau horaire prend effet pour la première fois.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328615"
---
# <a name="tzrule"></a><span data-ttu-id="835ea-103">TZRULE</span><span class="sxs-lookup"><span data-stu-id="835ea-103">TZRULE</span></span>

<span data-ttu-id="835ea-104">Spécifie les informations d’une règle de fuseau horaire concernant le début de l’heure d’été et l’année pendant laquelle cette règle de fuseau horaire prend effet pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="835ea-104">Specifies information for a time zone rule about when daylight saving time starts, and the year in which that time zone rule first takes effect.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="835ea-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="835ea-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a><span data-ttu-id="835ea-106">Membres</span><span class="sxs-lookup"><span data-stu-id="835ea-106">Members</span></span>

<span data-ttu-id="835ea-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="835ea-107">_wFlags_</span></span>
  
> <span data-ttu-id="835ea-108">Les indicateurs de ce membre identifient des détails spécifiques pour cette règle de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="835ea-108">The flags set for this member identify specific details for this time zone rule.</span></span> <span data-ttu-id="835ea-109">Les indicateurs possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="835ea-109">The possible flags are as follows:</span></span>
    
   - <span data-ttu-id="835ea-110">**TZRULE_FLAG_EFFECTIVE_TZREG** : identifie la règle comme celle qui doit être utilisée actuellement.</span><span class="sxs-lookup"><span data-stu-id="835ea-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —Identifies the rule as the one that should be used currently.</span></span> <span data-ttu-id="835ea-111">Une seule règle peut être marquée comme règle effective.</span><span class="sxs-lookup"><span data-stu-id="835ea-111">Only one rule can be marked as the effective rule.</span></span> <span data-ttu-id="835ea-112">Toutes les autres règles sont uniquement à des fins de comparaison.</span><span class="sxs-lookup"><span data-stu-id="835ea-112">All other rules are for comparison purposes only.</span></span> 
    
   - <span data-ttu-id="835ea-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** — Lors de réunions périodiques, identifie la règle comme correspondant à la règle dans [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="835ea-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** —On recurring meetings, identifies the rule as matching the rule in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span> <span data-ttu-id="835ea-114">Cela peut être utilisé pour détecter si **PidLidTimeZoneStruct** a été modifié de manière significative par un client hérité, qui ne serait autrement pas conscient de la nouvelle propriété plus complète.</span><span class="sxs-lookup"><span data-stu-id="835ea-114">This can be used to detect whether **PidLidTimeZoneStruct** has been modified significantly by a legacy client, which would be otherwise unaware of the new, more complete property.</span></span> 
    
<span data-ttu-id="835ea-115">_stStart_</span><span class="sxs-lookup"><span data-stu-id="835ea-115">_stStart_</span></span>
  
> <span data-ttu-id="835ea-116">Heure UTC (Temps universel coordonné) à l’heure de début de la règle de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="835ea-116">The time in Coordinated Universal Time (UTC) that the time zone rule started.</span></span>
    
<span data-ttu-id="835ea-117">_TZReg_</span><span class="sxs-lookup"><span data-stu-id="835ea-117">_TZReg_</span></span>
  
> <span data-ttu-id="835ea-118">Informations de fuseau horaire pour la règle de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="835ea-118">The time zone information for the time zone rule.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="835ea-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="835ea-119">Remarks</span></span>

<span data-ttu-id="835ea-120">Cette structure augmente [le TZREG](tzreg.md) en fournissant des informations supplémentaires indiquant à quel moment les règles de fuseau horaire prennent effet.</span><span class="sxs-lookup"><span data-stu-id="835ea-120">This structure augments [TZREG](tzreg.md) by providing additional information indicating when time zone rules take effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="835ea-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="835ea-121">See also</span></span>

- [<span data-ttu-id="835ea-122">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="835ea-122">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [<span data-ttu-id="835ea-123">Constantes (Outlook des API exportées)</span><span class="sxs-lookup"><span data-stu-id="835ea-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="835ea-124">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="835ea-124">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
- [<span data-ttu-id="835ea-125">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="835ea-125">TZDEFINITION</span></span>](tzdefinition.md)

