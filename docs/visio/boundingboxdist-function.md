---
title: BOUNDINGBOXDIST, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Renvoie la mesure de la partie spécifiée du cadre englobant de la forme.
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788179"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="7f952-103">BOUNDINGBOXDIST, fonction</span><span class="sxs-lookup"><span data-stu-id="7f952-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="7f952-104">Renvoie la mesure de la partie spécifiée du cadre englobant de la forme.</span><span class="sxs-lookup"><span data-stu-id="7f952-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="7f952-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="7f952-105">Version Information</span></span>

<span data-ttu-id="7f952-106">Version ajoutée : Visio 2010</span><span class="sxs-lookup"><span data-stu-id="7f952-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7f952-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f952-107">Syntax</span></span>

<span data-ttu-id="7f952-108">BOUNDINGBOXDIST (** *Index* **)</span><span class="sxs-lookup"><span data-stu-id="7f952-108">BOUNDINGBOXDIST(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7f952-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f952-109">Parameters</span></span>

|<span data-ttu-id="7f952-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="7f952-110">**Name**</span></span>|<span data-ttu-id="7f952-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="7f952-111">**Required/Optional**</span></span>|<span data-ttu-id="7f952-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="7f952-112">**Data Type**</span></span>|<span data-ttu-id="7f952-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="7f952-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7f952-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="7f952-114">_Index_</span></span> <br/> |<span data-ttu-id="7f952-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f952-115">Required</span></span>  <br/> |<span data-ttu-id="7f952-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="7f952-116">**Number**</span></span> <br/> |<span data-ttu-id="7f952-117">La partie de la forme englobant pour mesurer et retourner.</span><span class="sxs-lookup"><span data-stu-id="7f952-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="7f952-118">Voir la section Remarques pour les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="7f952-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7f952-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="7f952-119">Return value</span></span>

 <span data-ttu-id="7f952-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="7f952-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f952-121">Note</span><span class="sxs-lookup"><span data-stu-id="7f952-121">Remarks</span></span>

 <span data-ttu-id="7f952-122">*Index* peut être une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7f952-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="7f952-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="7f952-123">**Item**</span></span>|<span data-ttu-id="7f952-124">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7f952-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f952-125">Largeur</span><span class="sxs-lookup"><span data-stu-id="7f952-125">Width</span></span>  <br/> |<span data-ttu-id="7f952-126">0</span><span class="sxs-lookup"><span data-stu-id="7f952-126">0</span></span>  <br/> |
|<span data-ttu-id="7f952-127">Hauteur</span><span class="sxs-lookup"><span data-stu-id="7f952-127">Height</span></span>  <br/> |<span data-ttu-id="7f952-128">1</span><span class="sxs-lookup"><span data-stu-id="7f952-128">1</span></span>  <br/> |
|<span data-ttu-id="7f952-129">Bord gauche à l’axe de la forme</span><span class="sxs-lookup"><span data-stu-id="7f952-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="7f952-130">2</span><span class="sxs-lookup"><span data-stu-id="7f952-130">2</span></span>  <br/> |
|<span data-ttu-id="7f952-131">Axe de la forme au bord droit</span><span class="sxs-lookup"><span data-stu-id="7f952-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="7f952-132">3</span><span class="sxs-lookup"><span data-stu-id="7f952-132">3</span></span>  <br/> |
|<span data-ttu-id="7f952-133">Axe de la forme au bord supérieur</span><span class="sxs-lookup"><span data-stu-id="7f952-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="7f952-134">4</span><span class="sxs-lookup"><span data-stu-id="7f952-134">4</span></span>  <br/> |
|<span data-ttu-id="7f952-135">Bord inférieur à l’axe de la forme</span><span class="sxs-lookup"><span data-stu-id="7f952-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="7f952-136">5</span><span class="sxs-lookup"><span data-stu-id="7f952-136">5</span></span>  <br/> |
|<span data-ttu-id="7f952-137">Centre du cadre englobant à AxeX</span><span class="sxs-lookup"><span data-stu-id="7f952-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="7f952-138">6</span><span class="sxs-lookup"><span data-stu-id="7f952-138">6</span></span>  <br/> |
|<span data-ttu-id="7f952-139">Centre du cadre englobant à AxeY</span><span class="sxs-lookup"><span data-stu-id="7f952-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="7f952-140">7</span><span class="sxs-lookup"><span data-stu-id="7f952-140">7</span></span>  <br/> |
   

