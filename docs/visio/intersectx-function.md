---
title: INTERSECTX, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
localization_priority: Normal
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: Renvoie la coordonnée x (dans le système de coordonnées locales) du point d'intersection de deux lignes.
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418273"
---
# <a name="intersectx-function"></a><span data-ttu-id="c4a9d-103">Fonction INTERSECTX</span><span class="sxs-lookup"><span data-stu-id="c4a9d-103">INTERSECTX Function</span></span>

<span data-ttu-id="c4a9d-104">Renvoie la coordonnée *x* (dans le système de coordonnées locales) du point d'intersection de deux lignes.</span><span class="sxs-lookup"><span data-stu-id="c4a9d-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c4a9d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4a9d-105">Syntax</span></span>

<span data-ttu-id="c4a9d-106">INTERSECTX (\* \* *x1* \* \*, \* \* *Y1* \* \*, \* \* *angle1* \* \*, \* \* *x2* \* \*, \* \* *Y2* \* \*, \* \* *angle2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c4a9d-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c4a9d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4a9d-107">Parameters</span></span>

|<span data-ttu-id="c4a9d-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c4a9d-108">**Name**</span></span>|<span data-ttu-id="c4a9d-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="c4a9d-109">**Required/Optional**</span></span>|<span data-ttu-id="c4a9d-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="c4a9d-110">**Data Type**</span></span>|<span data-ttu-id="c4a9d-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c4a9d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c4a9d-112">_mâle_</span><span class="sxs-lookup"><span data-stu-id="c4a9d-112">_x1_</span></span> <br/> |<span data-ttu-id="c4a9d-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4a9d-113">Required</span></span>  <br/> |<span data-ttu-id="c4a9d-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="c4a9d-114">**Number**</span></span> <br/> |<span data-ttu-id="c4a9d-115">Coordonnée _x_d'un point sur la première ligne.</span><span class="sxs-lookup"><span data-stu-id="c4a9d-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="c4a9d-116">_Y1_</span><span class="sxs-lookup"><span data-stu-id="c4a9d-116">_y1_</span></span> <br/> |<span data-ttu-id="c4a9d-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4a9d-117">Required</span></span>  <br/> |<span data-ttu-id="c4a9d-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="c4a9d-118">**Number**</span></span> <br/> |<span data-ttu-id="c4a9d-119">Coordonnée _y_d'un point sur la première ligne.</span><span class="sxs-lookup"><span data-stu-id="c4a9d-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="c4a9d-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="c4a9d-120">_angle1_</span></span> <br/> |<span data-ttu-id="c4a9d-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4a9d-121">Required</span></span>  <br/> |<span data-ttu-id="c4a9d-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="c4a9d-122">**Number**</span></span> <br/> | <span data-ttu-id="c4a9d-123">Valeur de la cellule Angle de la première ligne.</span><span class="sxs-lookup"><span data-stu-id="c4a9d-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="c4a9d-124">_ports_</span><span class="sxs-lookup"><span data-stu-id="c4a9d-124">_x2_</span></span> <br/> |<span data-ttu-id="c4a9d-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4a9d-125">Required</span></span>  <br/> |<span data-ttu-id="c4a9d-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="c4a9d-126">**Number**</span></span> <br/> |<span data-ttu-id="c4a9d-127">Coordonnée _x_d'un point sur la deuxième ligne.</span><span class="sxs-lookup"><span data-stu-id="c4a9d-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="c4a9d-128">_Y2_</span><span class="sxs-lookup"><span data-stu-id="c4a9d-128">_y2_</span></span> <br/> |<span data-ttu-id="c4a9d-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4a9d-129">Required</span></span>  <br/> |<span data-ttu-id="c4a9d-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="c4a9d-130">**Number**</span></span> <br/> |<span data-ttu-id="c4a9d-131">Coordonnée _y_d'un point sur la deuxième ligne.</span><span class="sxs-lookup"><span data-stu-id="c4a9d-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="c4a9d-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="c4a9d-132">_angle2_</span></span> <br/> |<span data-ttu-id="c4a9d-133">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4a9d-133">Required</span></span>  <br/> |<span data-ttu-id="c4a9d-134">**Number**</span><span class="sxs-lookup"><span data-stu-id="c4a9d-134">**Number**</span></span> <br/> |<span data-ttu-id="c4a9d-135">Valeur de la cellule Angle de la deuxième ligne.</span><span class="sxs-lookup"><span data-stu-id="c4a9d-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c4a9d-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c4a9d-136">Return value</span></span>

<span data-ttu-id="c4a9d-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="c4a9d-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4a9d-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="c4a9d-138">Remarks</span></span>

<span data-ttu-id="c4a9d-139">Chaque ligne est définie par un point (*x,y*) et un angle.</span><span class="sxs-lookup"><span data-stu-id="c4a9d-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="c4a9d-140">Microsoft Visio utilise cette fonction dans la cellule PinX d’une forme collée à un repère retourné.</span><span class="sxs-lookup"><span data-stu-id="c4a9d-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="c4a9d-141">Si les lignes ne se coupent pas, la fonction renvoie une erreur Division par zéro (#DIV/0) que Visio ignore en restaurant la dernière valeur connue associée au point.</span><span class="sxs-lookup"><span data-stu-id="c4a9d-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c4a9d-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="c4a9d-142">Example</span></span>

<span data-ttu-id="c4a9d-143">INTERSECTX (RepèreVert! PinX, RepèreVert! PinY, RepèreVert! Angle, RepèreHoriz! PinX, RepèreHoriz! PinY, RepèreHoriz! Angle</span><span class="sxs-lookup"><span data-stu-id="c4a9d-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="c4a9d-144">Renvoie la coordonnée *x* du point d'intersection de RepèreVert et RepèreHoriz dans les unités de page.</span><span class="sxs-lookup"><span data-stu-id="c4a9d-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

