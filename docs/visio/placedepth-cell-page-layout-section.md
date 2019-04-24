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
ms.openlocfilehash: 463c7dad39955161538aa89d1482685189bf7fdc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346794"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="bdfb3-103">PlaceDepth, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="bdfb3-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="bdfb3-104">Détermine la méthode utilisée pour analyser le dessin avant la création de la mise en page et définit le type de mise en page.</span><span class="sxs-lookup"><span data-stu-id="bdfb3-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="bdfb3-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="bdfb3-105">**Value**</span></span>|<span data-ttu-id="bdfb3-106">**Profondeur de placement pour les mises en page verticales et horizontales**</span><span class="sxs-lookup"><span data-stu-id="bdfb3-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="bdfb3-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="bdfb3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="bdfb3-108">0</span><span class="sxs-lookup"><span data-stu-id="bdfb3-108">0</span></span>  <br/> | <span data-ttu-id="bdfb3-109">Valeur par défaut de la page</span><span class="sxs-lookup"><span data-stu-id="bdfb3-109">Page default</span></span>  <br/> |<span data-ttu-id="bdfb3-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="bdfb3-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="bdfb3-111">0,1</span><span class="sxs-lookup"><span data-stu-id="bdfb3-111">1</span></span>  <br/> | <span data-ttu-id="bdfb3-112">Moyenne</span><span class="sxs-lookup"><span data-stu-id="bdfb3-112">Medium</span></span>  <br/> |<span data-ttu-id="bdfb3-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="bdfb3-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="bdfb3-114">n°2</span><span class="sxs-lookup"><span data-stu-id="bdfb3-114">2</span></span>  <br/> | <span data-ttu-id="bdfb3-115">Développée</span><span class="sxs-lookup"><span data-stu-id="bdfb3-115">Deep</span></span>  <br/> |<span data-ttu-id="bdfb3-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="bdfb3-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="bdfb3-117">3</span><span class="sxs-lookup"><span data-stu-id="bdfb3-117">3</span></span>  <br/> | <span data-ttu-id="bdfb3-118">Partielle</span><span class="sxs-lookup"><span data-stu-id="bdfb3-118">Shallow</span></span>  <br/> |<span data-ttu-id="bdfb3-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="bdfb3-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdfb3-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="bdfb3-120">Remarks</span></span>

<span data-ttu-id="bdfb3-121">Pour obtenir une référence à la cellule PlaceDepth par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="bdfb3-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bdfb3-122">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bdfb3-122">Cell name:</span></span>  <br/> | <span data-ttu-id="bdfb3-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="bdfb3-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="bdfb3-124">Pour obtenir une référence à la cellule PlaceDepth à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bdfb3-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bdfb3-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bdfb3-125">Section index:</span></span>  <br/> |<span data-ttu-id="bdfb3-126">**Définis**</span><span class="sxs-lookup"><span data-stu-id="bdfb3-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bdfb3-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bdfb3-127">Row index:</span></span>  <br/> |<span data-ttu-id="bdfb3-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="bdfb3-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="bdfb3-129">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bdfb3-129">Cell index:</span></span>  <br/> |<span data-ttu-id="bdfb3-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="bdfb3-130">**visPLOPlaceDepth**</span></span> <br/> |
   

