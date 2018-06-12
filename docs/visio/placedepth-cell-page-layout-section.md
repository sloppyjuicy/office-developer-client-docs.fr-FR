---
title: PlaceDepth, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Détermine la méthode utilisée pour analyser le dessin avant la création de la mise en page et définit le type de mise en page.
ms.openlocfilehash: ab2c83a94c3dd03c1fdbf0c3ee187076406b2e84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789231"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="7ad98-103">PlaceDepth, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="7ad98-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="7ad98-104">Détermine la méthode utilisée pour analyser le dessin avant la création de la mise en page et définit le type de mise en page.</span><span class="sxs-lookup"><span data-stu-id="7ad98-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="7ad98-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7ad98-105">**Value**</span></span>|<span data-ttu-id="7ad98-106">**Profondeur de placement pour les mises en page verticales et horizontales**</span><span class="sxs-lookup"><span data-stu-id="7ad98-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="7ad98-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="7ad98-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7ad98-108">0</span><span class="sxs-lookup"><span data-stu-id="7ad98-108">0</span></span>  <br/> | <span data-ttu-id="7ad98-109">Valeur par défaut de la page</span><span class="sxs-lookup"><span data-stu-id="7ad98-109">Page default</span></span>  <br/> |<span data-ttu-id="7ad98-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="7ad98-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="7ad98-111">1</span><span class="sxs-lookup"><span data-stu-id="7ad98-111">1</span></span>  <br/> | <span data-ttu-id="7ad98-112">Moyen</span><span class="sxs-lookup"><span data-stu-id="7ad98-112">Medium</span></span>  <br/> |<span data-ttu-id="7ad98-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="7ad98-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="7ad98-114">2</span><span class="sxs-lookup"><span data-stu-id="7ad98-114">2</span></span>  <br/> | <span data-ttu-id="7ad98-115">Profond</span><span class="sxs-lookup"><span data-stu-id="7ad98-115">Deep</span></span>  <br/> |<span data-ttu-id="7ad98-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="7ad98-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="7ad98-117">3</span><span class="sxs-lookup"><span data-stu-id="7ad98-117">3</span></span>  <br/> | <span data-ttu-id="7ad98-118">Peu profond</span><span class="sxs-lookup"><span data-stu-id="7ad98-118">Shallow</span></span>  <br/> |<span data-ttu-id="7ad98-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="7ad98-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ad98-120">Note</span><span class="sxs-lookup"><span data-stu-id="7ad98-120">Remarks</span></span>

<span data-ttu-id="7ad98-121">Pour obtenir une référence à la cellule PlaceDepth par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="7ad98-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7ad98-122">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7ad98-122">Cell name:</span></span>  <br/> | <span data-ttu-id="7ad98-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="7ad98-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="7ad98-124">Pour obtenir une référence à la cellule PlaceDepth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7ad98-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7ad98-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7ad98-125">Section index:</span></span>  <br/> |<span data-ttu-id="7ad98-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7ad98-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7ad98-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7ad98-127">Row index:</span></span>  <br/> |<span data-ttu-id="7ad98-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="7ad98-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="7ad98-129">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7ad98-129">Cell index:</span></span>  <br/> |<span data-ttu-id="7ad98-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="7ad98-130">**visPLOPlaceDepth**</span></span> <br/> |
   

