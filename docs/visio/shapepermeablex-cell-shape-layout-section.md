---
title: ShapePermeableX, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Détermine si un connecteur peut se positionner horizontalement en traversant une forme positionnable.
ms.openlocfilehash: 1e0fe614b9401ea453b9c650ef9af3b4105b3805
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789647"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a><span data-ttu-id="c0316-103">ShapePermeableX, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="c0316-103">ShapePermeableX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="c0316-104">Détermine si un connecteur peut se positionner horizontalement en traversant une forme positionnable.</span><span class="sxs-lookup"><span data-stu-id="c0316-104">Determines whether a connector can route horizontally through a placeable shape.</span></span>
  
|<span data-ttu-id="c0316-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c0316-105">**Value**</span></span>|<span data-ttu-id="c0316-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0316-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0316-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c0316-107">TRUE</span></span>  <br/> |<span data-ttu-id="c0316-108">Permet aux connecteurs de se positionner horizontalement en traversant une forme positionnable.</span><span class="sxs-lookup"><span data-stu-id="c0316-108">Enable connectors to route horizontally through a placeable shape.</span></span>  <br/> |
|<span data-ttu-id="c0316-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c0316-109">FALSE</span></span>  <br/> |<span data-ttu-id="c0316-110">Ne permet pas aux connecteurs de se positionner horizontalement en traversant une forme positionnable.</span><span class="sxs-lookup"><span data-stu-id="c0316-110">Do not let connectors route horizontally through a placeable shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0316-111">Note</span><span class="sxs-lookup"><span data-stu-id="c0316-111">Remarks</span></span>

<span data-ttu-id="c0316-112">Vous pouvez également définir la valeur de cette cellule dans l’onglet **Placement** dans la boîte de dialogue **comportement** (avec la forme sélectionnée, sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe **Création de la forme** , cliquez sur **comportement**, puis cliquez sur l’onglet **Placement** ).</span><span class="sxs-lookup"><span data-stu-id="c0316-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="c0316-113">Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="c0316-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="c0316-114">Pour obtenir une référence à la cellule ShapePermeableX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c0316-114">To get a reference to the ShapePermeableX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0316-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c0316-115">Cell name:</span></span>  <br/> |<span data-ttu-id="c0316-116">ShapePermeableX</span><span class="sxs-lookup"><span data-stu-id="c0316-116">ShapePermeableX</span></span>  <br/> |
   
<span data-ttu-id="c0316-117">Pour obtenir une référence à la cellule ShapePermeableX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c0316-117">To get a reference to the ShapePermeableX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0316-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c0316-118">Section index:</span></span>  <br/> |<span data-ttu-id="c0316-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0316-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c0316-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c0316-120">Row index:</span></span>  <br/> |<span data-ttu-id="c0316-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="c0316-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="c0316-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c0316-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c0316-123">**visSLOPermX**</span><span class="sxs-lookup"><span data-stu-id="c0316-123">**visSLOPermX**</span></span> <br/> |
   

