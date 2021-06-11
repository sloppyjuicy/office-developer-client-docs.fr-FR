---
title: INTERSECTY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Renvoie la coordonnée y (dans le système de coordonnées local) du point où deux lignes se coupent.
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426099"
---
# <a name="intersecty-function"></a><span data-ttu-id="ac8fc-103">Fonction INTERSECTY</span><span class="sxs-lookup"><span data-stu-id="ac8fc-103">INTERSECTY Function</span></span>

<span data-ttu-id="ac8fc-104">Renvoie la  *coordonnée y*  (dans le système de coordonnées local) du point où deux lignes se coupent.</span><span class="sxs-lookup"><span data-stu-id="ac8fc-104">Returns the  *y*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ac8fc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac8fc-105">Syntax</span></span>

<span data-ttu-id="ac8fc-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ac8fc-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ac8fc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac8fc-107">Parameters</span></span>

|<span data-ttu-id="ac8fc-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ac8fc-108">**Name**</span></span>|<span data-ttu-id="ac8fc-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="ac8fc-109">**Required/Optional**</span></span>|<span data-ttu-id="ac8fc-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ac8fc-110">**Data Type**</span></span>|<span data-ttu-id="ac8fc-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ac8fc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ac8fc-112">_x1_</span><span class="sxs-lookup"><span data-stu-id="ac8fc-112">_x1_</span></span> <br/> |<span data-ttu-id="ac8fc-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ac8fc-113">Required</span></span>  <br/> |<span data-ttu-id="ac8fc-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="ac8fc-114">**Number**</span></span> <br/> |<span data-ttu-id="ac8fc-115">Coordonnée  _x_ d’un point sur la première ligne.</span><span class="sxs-lookup"><span data-stu-id="ac8fc-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="ac8fc-116">_y1_</span><span class="sxs-lookup"><span data-stu-id="ac8fc-116">_y1_</span></span> <br/> |<span data-ttu-id="ac8fc-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ac8fc-117">Required</span></span>  <br/> |<span data-ttu-id="ac8fc-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="ac8fc-118">**Number**</span></span> <br/> |<span data-ttu-id="ac8fc-119">Coordonnée  _y_ d’un point sur la première ligne.</span><span class="sxs-lookup"><span data-stu-id="ac8fc-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="ac8fc-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="ac8fc-120">_angle1_</span></span> <br/> |<span data-ttu-id="ac8fc-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ac8fc-121">Required</span></span>  <br/> |<span data-ttu-id="ac8fc-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="ac8fc-122">**Number**</span></span> <br/> | <span data-ttu-id="ac8fc-123">Valeur de la cellule Angle de la première ligne.</span><span class="sxs-lookup"><span data-stu-id="ac8fc-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="ac8fc-124">_x2_</span><span class="sxs-lookup"><span data-stu-id="ac8fc-124">_x2_</span></span> <br/> |<span data-ttu-id="ac8fc-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ac8fc-125">Required</span></span>  <br/> |<span data-ttu-id="ac8fc-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="ac8fc-126">**Number**</span></span> <br/> |<span data-ttu-id="ac8fc-127">Coordonnée  _x_ d’un point sur la deuxième ligne.</span><span class="sxs-lookup"><span data-stu-id="ac8fc-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="ac8fc-128">_y2_</span><span class="sxs-lookup"><span data-stu-id="ac8fc-128">_y2_</span></span> <br/> |<span data-ttu-id="ac8fc-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ac8fc-129">Required</span></span>  <br/> |<span data-ttu-id="ac8fc-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="ac8fc-130">**Number**</span></span> <br/> |<span data-ttu-id="ac8fc-131">Coordonnée  _y_ d’un point sur la deuxième ligne.</span><span class="sxs-lookup"><span data-stu-id="ac8fc-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="ac8fc-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="ac8fc-132">_angle2_</span></span> <br/> |<span data-ttu-id="ac8fc-133">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ac8fc-133">Required</span></span>  <br/> |<span data-ttu-id="ac8fc-134">**Number**</span><span class="sxs-lookup"><span data-stu-id="ac8fc-134">**Number**</span></span> <br/> |<span data-ttu-id="ac8fc-135">Valeur de la cellule Angle de la deuxième ligne.</span><span class="sxs-lookup"><span data-stu-id="ac8fc-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ac8fc-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ac8fc-136">Return value</span></span>

<span data-ttu-id="ac8fc-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac8fc-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ac8fc-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac8fc-138">Remarks</span></span>

<span data-ttu-id="ac8fc-139">Chaque ligne est définie par un point (*x,y*) et un angle.</span><span class="sxs-lookup"><span data-stu-id="ac8fc-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="ac8fc-140">Microsoft Visio utilise cette fonction dans la cellule PinY d’une forme collée à un repère retourné.</span><span class="sxs-lookup"><span data-stu-id="ac8fc-140">Microsoft Visio uses this function in the PinY cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="ac8fc-141">Si les lignes ne se coupent pas, la fonction renvoie une erreur Division par zéro (#DIV/0) que Visio ignore en restaurant la dernière valeur connue associée au point.</span><span class="sxs-lookup"><span data-stu-id="ac8fc-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ac8fc-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="ac8fc-142">Example</span></span>

<span data-ttu-id="ac8fc-143">INTERSECTY(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide ! PinX,HorzGuide! PinY,HorzGuide! Angle)</span><span class="sxs-lookup"><span data-stu-id="ac8fc-143">INTERSECTY(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="ac8fc-144">Renvoie la  *coordonnée y*  du point d’intersection de VertGuide et HorzGuide en unités de page.</span><span class="sxs-lookup"><span data-stu-id="ac8fc-144">Returns the  *y*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

