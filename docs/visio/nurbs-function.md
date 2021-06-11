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
description: Renvoie une ligne B-spline rationnelle nonuniforme (NURBS). Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438455"
---
# <a name="nurbs-function"></a><span data-ttu-id="78f18-104">Fonction NURBS</span><span class="sxs-lookup"><span data-stu-id="78f18-104">NURBS Function</span></span>

<span data-ttu-id="78f18-105">Renvoie une ligne B-spline rationnelle nonuniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="78f18-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="78f18-106">Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="78f18-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="78f18-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78f18-107">Syntax</span></span>

<span data-ttu-id="78f18-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span><span class="sxs-lookup"><span data-stu-id="78f18-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="78f18-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78f18-109">Parameters</span></span>

|<span data-ttu-id="78f18-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="78f18-110">**Name**</span></span>|<span data-ttu-id="78f18-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="78f18-111">**Required/Optional**</span></span>|<span data-ttu-id="78f18-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="78f18-112">**Data Type**</span></span>|<span data-ttu-id="78f18-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="78f18-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="78f18-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="78f18-114">_knotLast_</span></span> <br/> |<span data-ttu-id="78f18-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="78f18-115">Required</span></span>  <br/> |<span data-ttu-id="78f18-116">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="78f18-116">**string**</span></span> <br/> | <span data-ttu-id="78f18-117">Dernier nœud</span><span class="sxs-lookup"><span data-stu-id="78f18-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="78f18-118">_degré_</span><span class="sxs-lookup"><span data-stu-id="78f18-118">_degree_</span></span> <br/> |<span data-ttu-id="78f18-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="78f18-119">Required</span></span>  <br/> |<span data-ttu-id="78f18-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="78f18-120">**Numeric**</span></span> <br/> |<span data-ttu-id="78f18-121">Degré de la courbe Spline</span><span class="sxs-lookup"><span data-stu-id="78f18-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="78f18-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="78f18-122">_xType_</span></span> <br/> |<span data-ttu-id="78f18-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="78f18-123">Required</span></span>  <br/> |<span data-ttu-id="78f18-124">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="78f18-124">**Numeric**</span></span> <br/> |<span data-ttu-id="78f18-125">Indique comment interpréter les _données d’entrée x._</span><span class="sxs-lookup"><span data-stu-id="78f18-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="78f18-126">Si  _xType est_ 0, toutes les  _données d’entrée x_ sont interprétées comme un pourcentage de la largeur.</span><span class="sxs-lookup"><span data-stu-id="78f18-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="78f18-127">Si  _xType est_ 1, toutes les  _données d’entrée x_ sont interprétées comme des coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="78f18-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="78f18-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="78f18-128">_yType_</span></span> <br/> |<span data-ttu-id="78f18-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="78f18-129">Required</span></span>  <br/> |<span data-ttu-id="78f18-130">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="78f18-130">**Numeric**</span></span> <br/> |<span data-ttu-id="78f18-131">Indique comment interpréter les données _d’entrée y._</span><span class="sxs-lookup"><span data-stu-id="78f18-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="78f18-132">Si  _yType est_ 0, toutes les données d’entrée  _y_ sont interprétées comme un pourcentage de height.</span><span class="sxs-lookup"><span data-stu-id="78f18-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="78f18-133">Si  _yType est_ 1, toutes les données d’entrée  _y_ sont interprétées comme des coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="78f18-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="78f18-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="78f18-134">_x1_</span></span> <br/> |<span data-ttu-id="78f18-135">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="78f18-135">Required</span></span>  <br/> |<span data-ttu-id="78f18-136">**String**</span><span class="sxs-lookup"><span data-stu-id="78f18-136">**String**</span></span> <br/> |<span data-ttu-id="78f18-137">Coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="78f18-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="78f18-138">_y1_</span><span class="sxs-lookup"><span data-stu-id="78f18-138">_y1_</span></span> <br/> |<span data-ttu-id="78f18-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="78f18-139">Required</span></span>  <br/> |<span data-ttu-id="78f18-140">**String**</span><span class="sxs-lookup"><span data-stu-id="78f18-140">**String**</span></span> <br/> |<span data-ttu-id="78f18-141">Coordonnée y.</span><span class="sxs-lookup"><span data-stu-id="78f18-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="78f18-142">_nœud1_</span><span class="sxs-lookup"><span data-stu-id="78f18-142">_knot1_</span></span> <br/> |<span data-ttu-id="78f18-143">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="78f18-143">Required</span></span>  <br/> |<span data-ttu-id="78f18-144">**String**</span><span class="sxs-lookup"><span data-stu-id="78f18-144">**String**</span></span> <br/> |<span data-ttu-id="78f18-145">Nœud sur la courbe B-spline</span><span class="sxs-lookup"><span data-stu-id="78f18-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="78f18-146">_weight1_</span><span class="sxs-lookup"><span data-stu-id="78f18-146">_weight1_</span></span> <br/> |<span data-ttu-id="78f18-147">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="78f18-147">Required</span></span>  <br/> |<span data-ttu-id="78f18-148">**String**</span><span class="sxs-lookup"><span data-stu-id="78f18-148">**String**</span></span> <br/> |<span data-ttu-id="78f18-149">Épaisseur sur la courbe B-spline</span><span class="sxs-lookup"><span data-stu-id="78f18-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78f18-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="78f18-150">Remarks</span></span>

<span data-ttu-id="78f18-151">Pour chaque argument  *x,*  il doit y avoir un argument  *y*  ; Sinon, une erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="78f18-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="78f18-152">Vous devez spécifier au moins un *argument* *x*, *y*, *nœud* et poids ; sinon, Visio renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="78f18-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

