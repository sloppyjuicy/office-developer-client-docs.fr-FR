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
description: Renvoie le x-coordonnée (dans le système de coordonnées local) du point d’intersectent de deux lignes.
ms.openlocfilehash: ea5a08f25f3e45dab3fe3fd83b74cf9a7541b6e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788834"
---
# <a name="intersectx-function"></a><span data-ttu-id="ae6c0-103">INTERSECTX, fonction</span><span class="sxs-lookup"><span data-stu-id="ae6c0-103">INTERSECTX Function</span></span>

<span data-ttu-id="ae6c0-104">Renvoie le *x* -coordonnée (dans le système de coordonnées local) du point d’intersectent de deux lignes.</span><span class="sxs-lookup"><span data-stu-id="ae6c0-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ae6c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae6c0-105">Syntax</span></span>

<span data-ttu-id="ae6c0-106">INTERSECTX (** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* **)</span><span class="sxs-lookup"><span data-stu-id="ae6c0-106">INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ae6c0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae6c0-107">Parameters</span></span>

|<span data-ttu-id="ae6c0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ae6c0-108">**Name**</span></span>|<span data-ttu-id="ae6c0-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="ae6c0-109">**Required/Optional**</span></span>|<span data-ttu-id="ae6c0-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ae6c0-110">**Data Type**</span></span>|<span data-ttu-id="ae6c0-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ae6c0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ae6c0-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="ae6c0-112">_x1_</span></span> <br/> |<span data-ttu-id="ae6c0-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ae6c0-113">Required</span></span>  <br/> |<span data-ttu-id="ae6c0-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="ae6c0-114">**Number**</span></span> <br/> |<span data-ttu-id="ae6c0-115">_X_-coordonnées d’un point sur la première ligne.</span><span class="sxs-lookup"><span data-stu-id="ae6c0-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="ae6c0-116">_y1_</span><span class="sxs-lookup"><span data-stu-id="ae6c0-116">_y1_</span></span> <br/> |<span data-ttu-id="ae6c0-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ae6c0-117">Required</span></span>  <br/> |<span data-ttu-id="ae6c0-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="ae6c0-118">**Number**</span></span> <br/> |<span data-ttu-id="ae6c0-119">La valeur _y_-coordonnées d’un point sur la première ligne.</span><span class="sxs-lookup"><span data-stu-id="ae6c0-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="ae6c0-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="ae6c0-120">_angle1_</span></span> <br/> |<span data-ttu-id="ae6c0-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ae6c0-121">Required</span></span>  <br/> |<span data-ttu-id="ae6c0-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="ae6c0-122">**Number**</span></span> <br/> | <span data-ttu-id="ae6c0-123">Valeur de la cellule Angle de la première ligne.</span><span class="sxs-lookup"><span data-stu-id="ae6c0-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="ae6c0-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="ae6c0-124">_x2_</span></span> <br/> |<span data-ttu-id="ae6c0-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ae6c0-125">Required</span></span>  <br/> |<span data-ttu-id="ae6c0-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="ae6c0-126">**Number**</span></span> <br/> |<span data-ttu-id="ae6c0-127">_X_-coordonnées d’un point sur la deuxième ligne.</span><span class="sxs-lookup"><span data-stu-id="ae6c0-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="ae6c0-128">_y2_</span><span class="sxs-lookup"><span data-stu-id="ae6c0-128">_y2_</span></span> <br/> |<span data-ttu-id="ae6c0-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ae6c0-129">Required</span></span>  <br/> |<span data-ttu-id="ae6c0-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="ae6c0-130">**Number**</span></span> <br/> |<span data-ttu-id="ae6c0-131">La valeur _y_-coordonnées d’un point sur la deuxième ligne.</span><span class="sxs-lookup"><span data-stu-id="ae6c0-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="ae6c0-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="ae6c0-132">_angle2_</span></span> <br/> |<span data-ttu-id="ae6c0-133">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ae6c0-133">Required</span></span>  <br/> |<span data-ttu-id="ae6c0-134">**Number**</span><span class="sxs-lookup"><span data-stu-id="ae6c0-134">**Number**</span></span> <br/> |<span data-ttu-id="ae6c0-135">Valeur de la cellule Angle de la deuxième ligne.</span><span class="sxs-lookup"><span data-stu-id="ae6c0-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ae6c0-136">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="ae6c0-136">Return value</span></span>

<span data-ttu-id="ae6c0-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae6c0-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae6c0-138">Note</span><span class="sxs-lookup"><span data-stu-id="ae6c0-138">Remarks</span></span>

<span data-ttu-id="ae6c0-139">Chaque ligne est définie par un point (*x, y*) et un angle.</span><span class="sxs-lookup"><span data-stu-id="ae6c0-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="ae6c0-140">Microsoft Visio utilise cette fonction dans la cellule PinX d’une forme collée à un repère retourné.</span><span class="sxs-lookup"><span data-stu-id="ae6c0-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="ae6c0-141">Si les lignes ne se coupent pas, la fonction renvoie une erreur Division par zéro (#DIV/0) que Visio ignore en restaurant la dernière valeur connue associée au point.</span><span class="sxs-lookup"><span data-stu-id="ae6c0-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ae6c0-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="ae6c0-142">Example</span></span>

<span data-ttu-id="ae6c0-143">INTERSECTX (RepèreVert ! PinX, RepèreVert ! PinY, RepèreVert ! Angle, RepèreHoriz ! PinX, RepèreHoriz ! PinY, RepèreHoriz ! Angle)</span><span class="sxs-lookup"><span data-stu-id="ae6c0-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="ae6c0-144">Renvoie le *x* -coordonnées du point d’intersection de RepèreVert et RepèreHoriz en unités de page.</span><span class="sxs-lookup"><span data-stu-id="ae6c0-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

