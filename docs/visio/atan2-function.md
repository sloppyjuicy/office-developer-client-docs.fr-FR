---
title: ATAN2, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Renvoie l’angle entre le vecteur représenté par x, y et la direction de la x-axe. Le résultat est un nombre dans l’unité actuelle de mesure pour les angles.
ms.openlocfilehash: dfd62ce628a3a46ff14b3ffc3f07074a39c66e14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788018"
---
# <a name="atan2-function"></a><span data-ttu-id="d7556-104">ATAN2, fonction</span><span class="sxs-lookup"><span data-stu-id="d7556-104">ATAN2 Function</span></span>

<span data-ttu-id="d7556-105">Renvoie l’angle entre le vecteur représenté par *x, y* et la direction de la *x* -axe.</span><span class="sxs-lookup"><span data-stu-id="d7556-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="d7556-106">Le résultat est un nombre dans l’unité actuelle de mesure pour les angles.</span><span class="sxs-lookup"><span data-stu-id="d7556-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d7556-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7556-107">Syntax</span></span>

<span data-ttu-id="d7556-108">ATAN2 (** *y* **, ** *x* **)</span><span class="sxs-lookup"><span data-stu-id="d7556-108">ATAN2(** *y* **, ** *x* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d7556-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7556-109">Parameters</span></span>

|<span data-ttu-id="d7556-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="d7556-110">**Name**</span></span>|<span data-ttu-id="d7556-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="d7556-111">**Required/Optional**</span></span>|<span data-ttu-id="d7556-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="d7556-112">**Data Type**</span></span>|<span data-ttu-id="d7556-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="d7556-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d7556-114">_y_</span><span class="sxs-lookup"><span data-stu-id="d7556-114">_y_</span></span> <br/> |<span data-ttu-id="d7556-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d7556-115">Required</span></span>  <br/> |<span data-ttu-id="d7556-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="d7556-116">**Numeric**</span></span> <br/> |<span data-ttu-id="d7556-117">La valeur _y_-valeur du point.</span><span class="sxs-lookup"><span data-stu-id="d7556-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="d7556-118">_x_</span><span class="sxs-lookup"><span data-stu-id="d7556-118">_x_</span></span> <br/> |<span data-ttu-id="d7556-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d7556-119">Required</span></span>  <br/> |<span data-ttu-id="d7556-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="d7556-120">**Numeric**</span></span> <br/> |<span data-ttu-id="d7556-121">_X_-valeur du point.</span><span class="sxs-lookup"><span data-stu-id="d7556-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7556-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7556-122">Remarks</span></span>

<span data-ttu-id="d7556-123">L’arctangente est l’angle mesuré dans le sens inverse de la *x* positif-axe sur une ligne qui coupe l’origine (0,0) et le point représenté par les valeurs *x* et *y* .</span><span class="sxs-lookup"><span data-stu-id="d7556-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="d7556-124">Dans Microsoft Visio, ATAN2 (0,0) renvoie 0.</span><span class="sxs-lookup"><span data-stu-id="d7556-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="d7556-125">Pour forcer le résultat de la fonction ATAN2 dans une mesure d’angle différente, utilisez les fonctions DEG ou RAD.</span><span class="sxs-lookup"><span data-stu-id="d7556-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="d7556-126">La fonction ATAN2 est la fonction inverse de la fonction TAN.</span><span class="sxs-lookup"><span data-stu-id="d7556-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="d7556-127">La fonction ATAN2 renvoie l’angle dont angle est égale à *y* divisé par *x* .</span><span class="sxs-lookup"><span data-stu-id="d7556-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="d7556-128">Si ATAN2 (*y, x*) représente un angle dans un triangle, *y* est le « côté opposé » et *x* étant le « côté adjacent », la fonction peut être écrite comme ATAN2(opposite,adjacent).</span><span class="sxs-lookup"><span data-stu-id="d7556-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d7556-129">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="d7556-129">Example 1</span></span>

<span data-ttu-id="d7556-130">ATAN2(1.25,2.25)</span><span class="sxs-lookup"><span data-stu-id="d7556-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="d7556-131">Renvoie 29,0456 deg</span><span class="sxs-lookup"><span data-stu-id="d7556-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d7556-132">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="d7556-132">Example 2</span></span>

<span data-ttu-id="d7556-133">ATAN2(1,RACINE(3))</span><span class="sxs-lookup"><span data-stu-id="d7556-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="d7556-134">Renvoie 30 deg</span><span class="sxs-lookup"><span data-stu-id="d7556-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d7556-135">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="d7556-135">Example 3</span></span>

<span data-ttu-id="d7556-136">ATAN2(1,1)</span><span class="sxs-lookup"><span data-stu-id="d7556-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="d7556-137">Renvoie 45 deg</span><span class="sxs-lookup"><span data-stu-id="d7556-137">Returns 45 deg</span></span>
  

