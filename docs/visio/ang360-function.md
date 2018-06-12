---
title: ANG360, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Normalise un angle.
ms.openlocfilehash: 01092e06b55c73953417fe7d0fa1c9f74d668922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788013"
---
# <a name="ang360-function"></a><span data-ttu-id="eba2e-103">ANG360, fonction</span><span class="sxs-lookup"><span data-stu-id="eba2e-103">ANG360 Function</span></span>

<span data-ttu-id="eba2e-104">Normalise la plage d’un angle 0 \<= résultat \< 2PI radians (0 \<= résultat \< 360 degrés).</span><span class="sxs-lookup"><span data-stu-id="eba2e-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="eba2e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eba2e-105">Syntax</span></span>

<span data-ttu-id="eba2e-106">ANG360 (** *angle* **)</span><span class="sxs-lookup"><span data-stu-id="eba2e-106">ANG360(** *angle* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eba2e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eba2e-107">Parameters</span></span>

|<span data-ttu-id="eba2e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="eba2e-108">**Name**</span></span>|<span data-ttu-id="eba2e-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="eba2e-109">**Required/Optional**</span></span>|<span data-ttu-id="eba2e-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="eba2e-110">**Data Type**</span></span>|<span data-ttu-id="eba2e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="eba2e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eba2e-112">_angle_</span><span class="sxs-lookup"><span data-stu-id="eba2e-112">_angle_</span></span> <br/> |<span data-ttu-id="eba2e-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="eba2e-113">Required</span></span>  <br/> |<span data-ttu-id="eba2e-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="eba2e-114">**Numeric**</span></span> <br/> |<span data-ttu-id="eba2e-115">Angle à normaliser.</span><span class="sxs-lookup"><span data-stu-id="eba2e-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eba2e-116">Note</span><span class="sxs-lookup"><span data-stu-id="eba2e-116">Remarks</span></span>

<span data-ttu-id="eba2e-117">Si *angle* n’est pas spécifié à l’aide d’unités d’angle, elle est interprétée comme radians.</span><span class="sxs-lookup"><span data-stu-id="eba2e-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="eba2e-118">Si *angle* ne peut pas être converti en une valeur, un #VALUE !</span><span class="sxs-lookup"><span data-stu-id="eba2e-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="eba2e-119">erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="eba2e-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="eba2e-120">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="eba2e-120">Example 1</span></span>

<span data-ttu-id="eba2e-121">ANG360(395 deg)</span><span class="sxs-lookup"><span data-stu-id="eba2e-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="eba2e-122">Renvoie 35 deg</span><span class="sxs-lookup"><span data-stu-id="eba2e-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="eba2e-123">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="eba2e-123">Example 2</span></span>

<span data-ttu-id="eba2e-124">ANG360(-9,8 rad)</span><span class="sxs-lookup"><span data-stu-id="eba2e-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="eba2e-125">Renvoie 2,7664 rad</span><span class="sxs-lookup"><span data-stu-id="eba2e-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="eba2e-126">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="eba2e-126">Example 3</span></span>

<span data-ttu-id="eba2e-127">ANG360(45)</span><span class="sxs-lookup"><span data-stu-id="eba2e-127">ANG360(45)</span></span>
  
<span data-ttu-id="eba2e-128">Renvoie 58,31 deg (1,0177 rad)</span><span class="sxs-lookup"><span data-stu-id="eba2e-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

