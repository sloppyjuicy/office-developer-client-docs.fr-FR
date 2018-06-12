---
title: BOUNDINGBOXRECT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Renvoie les coordonnées du bord spécifié du cadre englobant de la forme.
ms.openlocfilehash: 2c850cb213ec0093ead53cd860f92e38da46f27e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788174"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="4674c-103">BOUNDINGBOXRECT, fonction</span><span class="sxs-lookup"><span data-stu-id="4674c-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="4674c-104">Renvoie les coordonnées du bord spécifié du cadre englobant de la forme.</span><span class="sxs-lookup"><span data-stu-id="4674c-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="4674c-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="4674c-105">Version Information</span></span>

<span data-ttu-id="4674c-106">Version ajoutée : Visio 2010</span><span class="sxs-lookup"><span data-stu-id="4674c-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4674c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4674c-107">Syntax</span></span>

<span data-ttu-id="4674c-108">BOUNDINGBOXRECT (** *Index* **)</span><span class="sxs-lookup"><span data-stu-id="4674c-108">BOUNDINGBOXRECT(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4674c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4674c-109">Parameters</span></span>

|<span data-ttu-id="4674c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="4674c-110">**Name**</span></span>|<span data-ttu-id="4674c-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="4674c-111">**Required/Optional**</span></span>|<span data-ttu-id="4674c-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="4674c-112">**Data Type**</span></span>|<span data-ttu-id="4674c-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="4674c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4674c-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="4674c-114">_Index_</span></span> <br/> |<span data-ttu-id="4674c-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4674c-115">Required</span></span>  <br/> |<span data-ttu-id="4674c-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="4674c-116">**Integer**</span></span> <br/> |<span data-ttu-id="4674c-p101">Bord du cadre englobant de la forme pour lequel récupérer les coordonnées. Voir la section Remarques pour les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="4674c-p101">The edge of the shape's bounding box for which to get the coordinate. See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4674c-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4674c-119">Return value</span></span>

 <span data-ttu-id="4674c-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="4674c-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4674c-121">Note</span><span class="sxs-lookup"><span data-stu-id="4674c-121">Remarks</span></span>

 <span data-ttu-id="4674c-122">*Index* peut être une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4674c-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="4674c-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="4674c-123">**Item**</span></span>|<span data-ttu-id="4674c-124">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4674c-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4674c-125">Bord gauche</span><span class="sxs-lookup"><span data-stu-id="4674c-125">Left edge</span></span>  <br/> |<span data-ttu-id="4674c-126">0</span><span class="sxs-lookup"><span data-stu-id="4674c-126">0</span></span>  <br/> |
|<span data-ttu-id="4674c-127">Bord droit</span><span class="sxs-lookup"><span data-stu-id="4674c-127">Right edge</span></span>  <br/> |<span data-ttu-id="4674c-128">1</span><span class="sxs-lookup"><span data-stu-id="4674c-128">1</span></span>  <br/> |
|<span data-ttu-id="4674c-129">Bord supérieur</span><span class="sxs-lookup"><span data-stu-id="4674c-129">Top edge</span></span>  <br/> |<span data-ttu-id="4674c-130">2</span><span class="sxs-lookup"><span data-stu-id="4674c-130">2</span></span>  <br/> |
|<span data-ttu-id="4674c-131">Bord inférieur</span><span class="sxs-lookup"><span data-stu-id="4674c-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="4674c-132">3</span><span class="sxs-lookup"><span data-stu-id="4674c-132">3</span></span>  <br/> |
   
<span data-ttu-id="4674c-133">Si la forme a un parent, la valeur renvoyée est dans le système de coordonnées de ce parent.</span><span class="sxs-lookup"><span data-stu-id="4674c-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

