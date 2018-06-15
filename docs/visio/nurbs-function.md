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
description: Renvoie une courbe B-spline rationnelle (NURBS). Cette fonction est utilisée dans la cellule E dans les lignes de géométrie NURBSTo.
ms.openlocfilehash: 005a66b9da2425beaf416ec2273c10446c183add
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789211"
---
# <a name="nurbs-function"></a><span data-ttu-id="0a3c9-104">NURBS, fonction</span><span class="sxs-lookup"><span data-stu-id="0a3c9-104">NURBS Function</span></span>

<span data-ttu-id="0a3c9-105">Renvoie une courbe B-spline rationnelle (NURBS).</span><span class="sxs-lookup"><span data-stu-id="0a3c9-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="0a3c9-106">Cette fonction est utilisée dans la cellule E dans les lignes de géométrie NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="0a3c9-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0a3c9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a3c9-107">Syntax</span></span>

<span data-ttu-id="0a3c9-108">NURBS (** *dernier nœud* **, ** *degré* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *nœud1* **, ** *épaisseur1* **,...)</span><span class="sxs-lookup"><span data-stu-id="0a3c9-108">NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0a3c9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a3c9-109">Parameters</span></span>

|<span data-ttu-id="0a3c9-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-110">**Name**</span></span>|<span data-ttu-id="0a3c9-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-111">**Required/Optional**</span></span>|<span data-ttu-id="0a3c9-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-112">**Data Type**</span></span>|<span data-ttu-id="0a3c9-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0a3c9-114">_dernier nœud_</span><span class="sxs-lookup"><span data-stu-id="0a3c9-114">_knotLast_</span></span> <br/> |<span data-ttu-id="0a3c9-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a3c9-115">Required</span></span>  <br/> |<span data-ttu-id="0a3c9-116">**string**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-116">**string**</span></span> <br/> | <span data-ttu-id="0a3c9-117">Dernier nœud</span><span class="sxs-lookup"><span data-stu-id="0a3c9-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="0a3c9-118">_degré_</span><span class="sxs-lookup"><span data-stu-id="0a3c9-118">_degree_</span></span> <br/> |<span data-ttu-id="0a3c9-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a3c9-119">Required</span></span>  <br/> |<span data-ttu-id="0a3c9-120">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-120">**Numeric**</span></span> <br/> |<span data-ttu-id="0a3c9-121">Degré de la courbe Spline</span><span class="sxs-lookup"><span data-stu-id="0a3c9-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="0a3c9-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="0a3c9-122">_xType_</span></span> <br/> |<span data-ttu-id="0a3c9-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a3c9-123">Required</span></span>  <br/> |<span data-ttu-id="0a3c9-124">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-124">**Numeric**</span></span> <br/> |<span data-ttu-id="0a3c9-125">Spécifie comment interpréter les données _x_ entrées.</span><span class="sxs-lookup"><span data-stu-id="0a3c9-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="0a3c9-126">Si _xType_ a la valeur 0, toutes les données d’entrée _x_ est interprétée comme un pourcentage de largeur.</span><span class="sxs-lookup"><span data-stu-id="0a3c9-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="0a3c9-127">Si _xType_ a la valeur 1, toutes les données d’entrée _x_ est interprétée comme des coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="0a3c9-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="0a3c9-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="0a3c9-128">_yType_</span></span> <br/> |<span data-ttu-id="0a3c9-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a3c9-129">Required</span></span>  <br/> |<span data-ttu-id="0a3c9-130">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-130">**Numeric**</span></span> <br/> |<span data-ttu-id="0a3c9-131">Spécifie comment interpréter les données _y_ entrées.</span><span class="sxs-lookup"><span data-stu-id="0a3c9-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="0a3c9-132">Si _yType_ a la valeur 0, toutes les données entrées _y_ est interprétée comme un pourcentage de hauteur.</span><span class="sxs-lookup"><span data-stu-id="0a3c9-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="0a3c9-133">Si _yType_ a la valeur 1, toutes les données entrées _y_ est interprétée comme des coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="0a3c9-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="0a3c9-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="0a3c9-134">_x1_</span></span> <br/> |<span data-ttu-id="0a3c9-135">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a3c9-135">Required</span></span>  <br/> |<span data-ttu-id="0a3c9-136">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-136">**String**</span></span> <br/> |<span data-ttu-id="0a3c9-137">Coordonnée x</span><span class="sxs-lookup"><span data-stu-id="0a3c9-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="0a3c9-138">_y1_</span><span class="sxs-lookup"><span data-stu-id="0a3c9-138">_y1_</span></span> <br/> |<span data-ttu-id="0a3c9-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a3c9-139">Required</span></span>  <br/> |<span data-ttu-id="0a3c9-140">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-140">**String**</span></span> <br/> |<span data-ttu-id="0a3c9-141">Coordonnée y</span><span class="sxs-lookup"><span data-stu-id="0a3c9-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="0a3c9-142">_Nœud1_</span><span class="sxs-lookup"><span data-stu-id="0a3c9-142">_knot1_</span></span> <br/> |<span data-ttu-id="0a3c9-143">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a3c9-143">Required</span></span>  <br/> |<span data-ttu-id="0a3c9-144">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-144">**String**</span></span> <br/> |<span data-ttu-id="0a3c9-145">Nœud sur la courbe B-spline</span><span class="sxs-lookup"><span data-stu-id="0a3c9-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="0a3c9-146">_épaisseur1_</span><span class="sxs-lookup"><span data-stu-id="0a3c9-146">_weight1_</span></span> <br/> |<span data-ttu-id="0a3c9-147">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a3c9-147">Required</span></span>  <br/> |<span data-ttu-id="0a3c9-148">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="0a3c9-148">**String**</span></span> <br/> |<span data-ttu-id="0a3c9-149">Épaisseur sur la courbe B-spline</span><span class="sxs-lookup"><span data-stu-id="0a3c9-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a3c9-150">Note</span><span class="sxs-lookup"><span data-stu-id="0a3c9-150">Remarks</span></span>

<span data-ttu-id="0a3c9-151">Pour chaque argument *x* , il doit exister un argument *y* ; dans le cas contraire, une erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="0a3c9-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="0a3c9-152">Vous devez spécifier au moins un *x*, *y*, *nœud* et *épaisseur* argument ; dans le cas contraire, Visio renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="0a3c9-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

