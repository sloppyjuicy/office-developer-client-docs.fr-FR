---
title: NURBS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Renvoie une courbe B-spline rationnelle inuniforme (NURBS). Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340123"
---
# <a name="nurbs-function"></a><span data-ttu-id="dbada-104">Fonction NURBS</span><span class="sxs-lookup"><span data-stu-id="dbada-104">NURBS Function</span></span>

<span data-ttu-id="dbada-105">Renvoie une courbe B-spline rationnelle inuniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="dbada-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="dbada-106">Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="dbada-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dbada-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbada-107">Syntax</span></span>

<span data-ttu-id="dbada-108">NURBS (\* \* *knotLast* \* \*, \* \* *degree* \* *, \* \*\* xtype* \* \*, \* \* *yType* \* *, \* \*\* x1* \* \*, \* \* *Y1* \* \*, \* \* *knot1* \* \*, \* \* *Weight1* \* \*,...)</span><span class="sxs-lookup"><span data-stu-id="dbada-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dbada-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbada-109">Parameters</span></span>

|<span data-ttu-id="dbada-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="dbada-110">**Name**</span></span>|<span data-ttu-id="dbada-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="dbada-111">**Required/Optional**</span></span>|<span data-ttu-id="dbada-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="dbada-112">**Data Type**</span></span>|<span data-ttu-id="dbada-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="dbada-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dbada-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="dbada-114">_knotLast_</span></span> <br/> |<span data-ttu-id="dbada-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dbada-115">Required</span></span>  <br/> |<span data-ttu-id="dbada-116">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="dbada-116">**string**</span></span> <br/> | <span data-ttu-id="dbada-117">Dernier nœud</span><span class="sxs-lookup"><span data-stu-id="dbada-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="dbada-118">_degré_</span><span class="sxs-lookup"><span data-stu-id="dbada-118">_degree_</span></span> <br/> |<span data-ttu-id="dbada-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dbada-119">Required</span></span>  <br/> |<span data-ttu-id="dbada-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="dbada-120">**Numeric**</span></span> <br/> |<span data-ttu-id="dbada-121">Degré de la courbe Spline</span><span class="sxs-lookup"><span data-stu-id="dbada-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="dbada-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="dbada-122">_xType_</span></span> <br/> |<span data-ttu-id="dbada-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dbada-123">Required</span></span>  <br/> |<span data-ttu-id="dbada-124">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="dbada-124">**Numeric**</span></span> <br/> |<span data-ttu-id="dbada-125">Indique comment interpréter les données _x_ d'entrée.</span><span class="sxs-lookup"><span data-stu-id="dbada-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="dbada-126">Si _xtype_ a la valeur 0, toutes les données d'entrée _x_ sont interprétées comme un pourcentage de la largeur.</span><span class="sxs-lookup"><span data-stu-id="dbada-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="dbada-127">Si _xtype_ a la forme 1, toutes les données _x_ d'entrée sont interprétées comme des coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="dbada-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="dbada-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="dbada-128">_yType_</span></span> <br/> |<span data-ttu-id="dbada-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dbada-129">Required</span></span>  <br/> |<span data-ttu-id="dbada-130">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="dbada-130">**Numeric**</span></span> <br/> |<span data-ttu-id="dbada-131">Indique comment interpréter les données d'entrée _y_ .</span><span class="sxs-lookup"><span data-stu-id="dbada-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="dbada-132">Si _yType_ a la valeur 0, toutes les données _y_ d'entrée sont interprétées comme un pourcentage de la hauteur.</span><span class="sxs-lookup"><span data-stu-id="dbada-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="dbada-133">Si _yType_ a la valeurs 1, toutes les données _y_ d'entrée sont interprétées comme des coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="dbada-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="dbada-134">_mâle_</span><span class="sxs-lookup"><span data-stu-id="dbada-134">_x1_</span></span> <br/> |<span data-ttu-id="dbada-135">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dbada-135">Required</span></span>  <br/> |<span data-ttu-id="dbada-136">**String**</span><span class="sxs-lookup"><span data-stu-id="dbada-136">**String**</span></span> <br/> |<span data-ttu-id="dbada-137">Coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="dbada-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="dbada-138">_Y1_</span><span class="sxs-lookup"><span data-stu-id="dbada-138">_y1_</span></span> <br/> |<span data-ttu-id="dbada-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dbada-139">Required</span></span>  <br/> |<span data-ttu-id="dbada-140">**String**</span><span class="sxs-lookup"><span data-stu-id="dbada-140">**String**</span></span> <br/> |<span data-ttu-id="dbada-141">Coordonnée y.</span><span class="sxs-lookup"><span data-stu-id="dbada-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="dbada-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="dbada-142">_knot1_</span></span> <br/> |<span data-ttu-id="dbada-143">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dbada-143">Required</span></span>  <br/> |<span data-ttu-id="dbada-144">**String**</span><span class="sxs-lookup"><span data-stu-id="dbada-144">**String**</span></span> <br/> |<span data-ttu-id="dbada-145">Nœud sur la courbe B-spline</span><span class="sxs-lookup"><span data-stu-id="dbada-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="dbada-146">_Weight1_</span><span class="sxs-lookup"><span data-stu-id="dbada-146">_weight1_</span></span> <br/> |<span data-ttu-id="dbada-147">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dbada-147">Required</span></span>  <br/> |<span data-ttu-id="dbada-148">**String**</span><span class="sxs-lookup"><span data-stu-id="dbada-148">**String**</span></span> <br/> |<span data-ttu-id="dbada-149">Épaisseur sur la courbe B-spline</span><span class="sxs-lookup"><span data-stu-id="dbada-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbada-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="dbada-150">Remarks</span></span>

<span data-ttu-id="dbada-151">Pour chaque argument *x* , il doit y avoir un argument *y* ; Sinon, une erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="dbada-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="dbada-152">Vous devez spécifier au moins un argument *x*, *y*, *nœud* et *poids* ; dans le cas contraire, Visio renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="dbada-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

