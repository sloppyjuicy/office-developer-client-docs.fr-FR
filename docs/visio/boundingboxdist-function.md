---
title: BOUNDINGBOXDIST, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Renvoie la mesure de la partie spécifiée du cadre englobant de la forme.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428276"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="67889-103">Fonction BOUNDINGBOXDIST</span><span class="sxs-lookup"><span data-stu-id="67889-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="67889-104">Renvoie la mesure de la partie spécifiée du cadre englobant de la forme.</span><span class="sxs-lookup"><span data-stu-id="67889-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="67889-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="67889-105">Version Information</span></span>

<span data-ttu-id="67889-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="67889-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="67889-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67889-107">Syntax</span></span>

<span data-ttu-id="67889-108">BOUNDINGBOXDIST (\* \* *index* \* \*)</span><span class="sxs-lookup"><span data-stu-id="67889-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="67889-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67889-109">Parameters</span></span>

|<span data-ttu-id="67889-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="67889-110">**Name**</span></span>|<span data-ttu-id="67889-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="67889-111">**Required/Optional**</span></span>|<span data-ttu-id="67889-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="67889-112">**Data Type**</span></span>|<span data-ttu-id="67889-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="67889-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="67889-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="67889-114">_Index_</span></span> <br/> |<span data-ttu-id="67889-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="67889-115">Required</span></span>  <br/> |<span data-ttu-id="67889-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="67889-116">**Number**</span></span> <br/> |<span data-ttu-id="67889-117">Partie de la zone de délimitation de la forme à mesurer et à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="67889-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="67889-118">Les valeurs possibles, reportez-vous à la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="67889-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="67889-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="67889-119">Return value</span></span>

 <span data-ttu-id="67889-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="67889-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67889-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="67889-121">Remarks</span></span>

 <span data-ttu-id="67889-122">*Index* peut prendre l'une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="67889-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="67889-123">**Élément**</span><span class="sxs-lookup"><span data-stu-id="67889-123">**Item**</span></span>|<span data-ttu-id="67889-124">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="67889-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="67889-125">Largeur</span><span class="sxs-lookup"><span data-stu-id="67889-125">Width</span></span>  <br/> |<span data-ttu-id="67889-126">0</span><span class="sxs-lookup"><span data-stu-id="67889-126">0</span></span>  <br/> |
|<span data-ttu-id="67889-127">Hauteur</span><span class="sxs-lookup"><span data-stu-id="67889-127">Height</span></span>  <br/> |<span data-ttu-id="67889-128">0,1</span><span class="sxs-lookup"><span data-stu-id="67889-128">1</span></span>  <br/> |
|<span data-ttu-id="67889-129">Bord gauche à l’axe de la forme</span><span class="sxs-lookup"><span data-stu-id="67889-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="67889-130">n°2</span><span class="sxs-lookup"><span data-stu-id="67889-130">2</span></span>  <br/> |
|<span data-ttu-id="67889-131">Axe de la forme au bord droit</span><span class="sxs-lookup"><span data-stu-id="67889-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="67889-132">3</span><span class="sxs-lookup"><span data-stu-id="67889-132">3</span></span>  <br/> |
|<span data-ttu-id="67889-133">Axe de la forme au bord supérieur</span><span class="sxs-lookup"><span data-stu-id="67889-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="67889-134">4</span><span class="sxs-lookup"><span data-stu-id="67889-134">4</span></span>  <br/> |
|<span data-ttu-id="67889-135">Bord inférieur à l’axe de la forme</span><span class="sxs-lookup"><span data-stu-id="67889-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="67889-136">disque</span><span class="sxs-lookup"><span data-stu-id="67889-136">5</span></span>  <br/> |
|<span data-ttu-id="67889-137">Centre du cadre englobant à AxeX</span><span class="sxs-lookup"><span data-stu-id="67889-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="67889-138">6.x</span><span class="sxs-lookup"><span data-stu-id="67889-138">6</span></span>  <br/> |
|<span data-ttu-id="67889-139">Centre du cadre englobant à AxeY</span><span class="sxs-lookup"><span data-stu-id="67889-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="67889-140">7j/7</span><span class="sxs-lookup"><span data-stu-id="67889-140">7</span></span>  <br/> |
   

