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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438455"
---
# <a name="nurbs-function"></a><span data-ttu-id="1dd2d-104">Fonction NURBS</span><span class="sxs-lookup"><span data-stu-id="1dd2d-104">NURBS Function</span></span>

<span data-ttu-id="1dd2d-105">Renvoie une courbe B-spline rationnelle inuniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="1dd2d-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="1dd2d-106">Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1dd2d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1dd2d-107">Syntax</span></span>

<span data-ttu-id="1dd2d-108">NURBS (\* \* *knotLast* \* \*, \* \* *degree* \* *, \* \*\* xtype* \* \*, \* \* *yType* \* *, \* \*\* x1* \* \*, \* \* *Y1* \* \*, \* \* *knot1* \* \*, \* \* *Weight1* \* \*,...)</span><span class="sxs-lookup"><span data-stu-id="1dd2d-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1dd2d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1dd2d-109">Parameters</span></span>

|<span data-ttu-id="1dd2d-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-110">**Name**</span></span>|<span data-ttu-id="1dd2d-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-111">**Required/Optional**</span></span>|<span data-ttu-id="1dd2d-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-112">**Data Type**</span></span>|<span data-ttu-id="1dd2d-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1dd2d-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="1dd2d-114">_knotLast_</span></span> <br/> |<span data-ttu-id="1dd2d-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1dd2d-115">Required</span></span>  <br/> |<span data-ttu-id="1dd2d-116">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-116">**string**</span></span> <br/> | <span data-ttu-id="1dd2d-117">Dernier nœud</span><span class="sxs-lookup"><span data-stu-id="1dd2d-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="1dd2d-118">_degré_</span><span class="sxs-lookup"><span data-stu-id="1dd2d-118">_degree_</span></span> <br/> |<span data-ttu-id="1dd2d-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1dd2d-119">Required</span></span>  <br/> |<span data-ttu-id="1dd2d-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-120">**Numeric**</span></span> <br/> |<span data-ttu-id="1dd2d-121">Degré de la courbe Spline</span><span class="sxs-lookup"><span data-stu-id="1dd2d-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="1dd2d-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="1dd2d-122">_xType_</span></span> <br/> |<span data-ttu-id="1dd2d-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1dd2d-123">Required</span></span>  <br/> |<span data-ttu-id="1dd2d-124">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-124">**Numeric**</span></span> <br/> |<span data-ttu-id="1dd2d-125">Indique comment interpréter les données _x_ d'entrée.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="1dd2d-126">Si _xtype_ a la valeur 0, toutes les données d'entrée _x_ sont interprétées comme un pourcentage de la largeur.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="1dd2d-127">Si _xtype_ a la forme 1, toutes les données _x_ d'entrée sont interprétées comme des coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="1dd2d-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="1dd2d-128">_yType_</span></span> <br/> |<span data-ttu-id="1dd2d-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1dd2d-129">Required</span></span>  <br/> |<span data-ttu-id="1dd2d-130">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-130">**Numeric**</span></span> <br/> |<span data-ttu-id="1dd2d-131">Indique comment interpréter les données d'entrée _y_ .</span><span class="sxs-lookup"><span data-stu-id="1dd2d-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="1dd2d-132">Si _yType_ a la valeur 0, toutes les données _y_ d'entrée sont interprétées comme un pourcentage de la hauteur.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="1dd2d-133">Si _yType_ a la valeurs 1, toutes les données _y_ d'entrée sont interprétées comme des coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="1dd2d-134">_mâle_</span><span class="sxs-lookup"><span data-stu-id="1dd2d-134">_x1_</span></span> <br/> |<span data-ttu-id="1dd2d-135">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1dd2d-135">Required</span></span>  <br/> |<span data-ttu-id="1dd2d-136">**String**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-136">**String**</span></span> <br/> |<span data-ttu-id="1dd2d-137">Coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="1dd2d-138">_Y1_</span><span class="sxs-lookup"><span data-stu-id="1dd2d-138">_y1_</span></span> <br/> |<span data-ttu-id="1dd2d-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1dd2d-139">Required</span></span>  <br/> |<span data-ttu-id="1dd2d-140">**String**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-140">**String**</span></span> <br/> |<span data-ttu-id="1dd2d-141">Coordonnée y.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="1dd2d-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="1dd2d-142">_knot1_</span></span> <br/> |<span data-ttu-id="1dd2d-143">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1dd2d-143">Required</span></span>  <br/> |<span data-ttu-id="1dd2d-144">**String**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-144">**String**</span></span> <br/> |<span data-ttu-id="1dd2d-145">Nœud sur la courbe B-spline</span><span class="sxs-lookup"><span data-stu-id="1dd2d-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="1dd2d-146">_Weight1_</span><span class="sxs-lookup"><span data-stu-id="1dd2d-146">_weight1_</span></span> <br/> |<span data-ttu-id="1dd2d-147">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1dd2d-147">Required</span></span>  <br/> |<span data-ttu-id="1dd2d-148">**String**</span><span class="sxs-lookup"><span data-stu-id="1dd2d-148">**String**</span></span> <br/> |<span data-ttu-id="1dd2d-149">Épaisseur sur la courbe B-spline</span><span class="sxs-lookup"><span data-stu-id="1dd2d-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1dd2d-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="1dd2d-150">Remarks</span></span>

<span data-ttu-id="1dd2d-151">Pour chaque argument *x* , il doit y avoir un argument *y* ; Sinon, une erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="1dd2d-152">Vous devez spécifier au moins un argument *x*, *y*, *nœud* et *poids* ; dans le cas contraire, Visio renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="1dd2d-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

