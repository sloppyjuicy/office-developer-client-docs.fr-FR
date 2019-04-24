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
description: Renvoie l'angle entre le vecteur représenté par x, y et la direction de l'axe des abscisses. Le résultat est un nombre exprimé dans l’unité actuelle de mesure des angles.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341481"
---
# <a name="atan2-function"></a><span data-ttu-id="636c8-104">Fonction ATAN2</span><span class="sxs-lookup"><span data-stu-id="636c8-104">ATAN2 Function</span></span>

<span data-ttu-id="636c8-105">Renvoie l'angle entre le vecteur représenté par *x, y* et la direction de l' \*\* axe des abscisses.</span><span class="sxs-lookup"><span data-stu-id="636c8-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="636c8-106">Le résultat est un nombre exprimé dans l’unité actuelle de mesure des angles.</span><span class="sxs-lookup"><span data-stu-id="636c8-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="636c8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="636c8-107">Syntax</span></span>

<span data-ttu-id="636c8-108">ATAN2 (\* \* *y* \* \*, \* \* *x* \* \*)</span><span class="sxs-lookup"><span data-stu-id="636c8-108">ATAN2(\*\* *y* \*\*, \*\* *x* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="636c8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="636c8-109">Parameters</span></span>

|<span data-ttu-id="636c8-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="636c8-110">**Name**</span></span>|<span data-ttu-id="636c8-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="636c8-111">**Required/Optional**</span></span>|<span data-ttu-id="636c8-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="636c8-112">**Data Type**</span></span>|<span data-ttu-id="636c8-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="636c8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="636c8-114">_y_</span><span class="sxs-lookup"><span data-stu-id="636c8-114">_y_</span></span> <br/> |<span data-ttu-id="636c8-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636c8-115">Required</span></span>  <br/> |<span data-ttu-id="636c8-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="636c8-116">**Numeric**</span></span> <br/> |<span data-ttu-id="636c8-117">Valeur _y_du point.</span><span class="sxs-lookup"><span data-stu-id="636c8-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="636c8-118">_x_</span><span class="sxs-lookup"><span data-stu-id="636c8-118">_x_</span></span> <br/> |<span data-ttu-id="636c8-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="636c8-119">Required</span></span>  <br/> |<span data-ttu-id="636c8-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="636c8-120">**Numeric**</span></span> <br/> |<span data-ttu-id="636c8-121">Valeur _x_du point.</span><span class="sxs-lookup"><span data-stu-id="636c8-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="636c8-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="636c8-122">Remarks</span></span>

<span data-ttu-id="636c8-123">L'arctangente est l'angle mesuré dans le sens des aiguilles d'une passe à partir de l'axe *x* positif vers une ligne qui coupe l'origine (0,0) et le point représenté par *x* et *y* .</span><span class="sxs-lookup"><span data-stu-id="636c8-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="636c8-124">Dans Microsoft Visio, ATAN2(0,0) renvoie 0.</span><span class="sxs-lookup"><span data-stu-id="636c8-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="636c8-125">Pour exprimer le résultat de la fonction ATAN2 dans une unité de mesure d’angle différente, utilisez les fonctions DEG ou RAD.</span><span class="sxs-lookup"><span data-stu-id="636c8-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="636c8-126">La fonction ATAN2 est l'antifonction de la fonction TAN.</span><span class="sxs-lookup"><span data-stu-id="636c8-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="636c8-127">La fonction ATAN2 renvoie l'angle dont l'angle est égal à *y* divisé par *x* .</span><span class="sxs-lookup"><span data-stu-id="636c8-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="636c8-128">Si ATAN2 (*y, x*) représente un angle dans un triangle droit, *y* le «côté opposé» et *x* le «côté adjacent», de sorte que la fonction peut être écrite sous la forme atan2 (opposé, adjacent).</span><span class="sxs-lookup"><span data-stu-id="636c8-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="636c8-129">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="636c8-129">Example 1</span></span>

<span data-ttu-id="636c8-130">ATAN2 (1,25, 2,25)</span><span class="sxs-lookup"><span data-stu-id="636c8-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="636c8-131">Renvoie 29,0456 deg</span><span class="sxs-lookup"><span data-stu-id="636c8-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="636c8-132">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="636c8-132">Example 2</span></span>

<span data-ttu-id="636c8-133">ATAN2 (1, SQRT (3))</span><span class="sxs-lookup"><span data-stu-id="636c8-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="636c8-134">Renvoie 30 deg</span><span class="sxs-lookup"><span data-stu-id="636c8-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="636c8-135">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="636c8-135">Example 3</span></span>

<span data-ttu-id="636c8-136">ATAN2 (1,1)</span><span class="sxs-lookup"><span data-stu-id="636c8-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="636c8-137">Renvoie 45 deg</span><span class="sxs-lookup"><span data-stu-id="636c8-137">Returns 45 deg</span></span>
  

