---
title: ASIN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Renvoie l’arc sinus d’un nombre, par exemple, l’angle dont le sinus est nombre.
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788054"
---
# <a name="asin-function"></a><span data-ttu-id="fc88d-103">ASIN, fonction</span><span class="sxs-lookup"><span data-stu-id="fc88d-103">ASIN Function</span></span>

<span data-ttu-id="fc88d-104">Renvoie l’arc sinus d’un nombre, par exemple, l’angle dont le sinus est *nombre* .</span><span class="sxs-lookup"><span data-stu-id="fc88d-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fc88d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc88d-105">Syntax</span></span>

<span data-ttu-id="fc88d-106">ASIN (** *numéro* **)</span><span class="sxs-lookup"><span data-stu-id="fc88d-106">ASIN(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fc88d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc88d-107">Parameters</span></span>

|<span data-ttu-id="fc88d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fc88d-108">**Name**</span></span>|<span data-ttu-id="fc88d-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="fc88d-109">**Required/Optional**</span></span>|<span data-ttu-id="fc88d-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="fc88d-110">**Data Type**</span></span>|<span data-ttu-id="fc88d-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="fc88d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fc88d-112">_number_</span><span class="sxs-lookup"><span data-stu-id="fc88d-112">_number_</span></span> <br/> |<span data-ttu-id="fc88d-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fc88d-113">Required</span></span>  <br/> |<span data-ttu-id="fc88d-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="fc88d-114">**Numeric**</span></span> <br/> |<span data-ttu-id="fc88d-115">Sinus de l’angle.</span><span class="sxs-lookup"><span data-stu-id="fc88d-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc88d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc88d-116">Remarks</span></span>

<span data-ttu-id="fc88d-117">La valeur entrée doit être dans la plage -1 < = *nombre* < = 1 ou un #NUM !</span><span class="sxs-lookup"><span data-stu-id="fc88d-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="fc88d-118">erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="fc88d-118">error is returned.</span></span> <span data-ttu-id="fc88d-119">L’angle obtenu se situe dans la plage -PI/2 < = *angle* < = PI/2 radians (-90 < = *angle* < = 90 degrés).</span><span class="sxs-lookup"><span data-stu-id="fc88d-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="fc88d-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="fc88d-120">Example</span></span>

<span data-ttu-id="fc88d-121">ASIN(1)</span><span class="sxs-lookup"><span data-stu-id="fc88d-121">ASIN(1)</span></span>
  
<span data-ttu-id="fc88d-122">Renvoie 90 deg</span><span class="sxs-lookup"><span data-stu-id="fc88d-122">Returns 90 deg</span></span>
  

