---
title: Snap, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
localization_priority: Normal
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: Détermine si d'autres formes peuvent être alignées sur les formes attribuées au calque. Les formes associées au calque peuvent être alignées sur d'autres formes, mais les autres formes ne peuvent pas être alignées sur elles.
ms.openlocfilehash: 87e7e7500469fb7f8c7fdd4771a0225d0e4fc993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359807"
---
# <a name="snap-cell-layers-section"></a><span data-ttu-id="bccde-104">Snap, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="bccde-104">Snap Cell (Layers Section)</span></span>

<span data-ttu-id="bccde-p102">Détermine si d'autres formes peuvent être alignées sur les formes attribuées au calque. Les formes associées au calque peuvent être alignées sur d'autres formes, mais les autres formes ne peuvent pas être alignées sur elles.</span><span class="sxs-lookup"><span data-stu-id="bccde-p102">Determines whether other shapes can snap to shapes assigned to the layer. Shapes assigned to the layer can snap to other shapes, but other shapes can't snap to them.</span></span>
  
|<span data-ttu-id="bccde-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="bccde-107">**Value**</span></span>|<span data-ttu-id="bccde-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="bccde-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bccde-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="bccde-109">TRUE</span></span>  <br/> |<span data-ttu-id="bccde-110">Les autres formes peuvent s'aligner sur les formes du calque.</span><span class="sxs-lookup"><span data-stu-id="bccde-110">Other shapes can snap to shapes on the layer.</span></span>  <br/> |
|<span data-ttu-id="bccde-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="bccde-111">FALSE</span></span>  <br/> |<span data-ttu-id="bccde-112">Les autres formes ne peuvent pas s'aligner sur les formes du calque.</span><span class="sxs-lookup"><span data-stu-id="bccde-112">Other shapes cannot snap to shapes on the layer.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bccde-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="bccde-113">Remarks</span></span>

<span data-ttu-id="bccde-114">Vous pouvez également définir la valeur de cette cellule à l’aide de l’option **Alignement** dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **Accueil**, dans le groupe **Modification**, cliquez sur **Calques**, puis sur **Propriétés des calques**).</span><span class="sxs-lookup"><span data-stu-id="bccde-114">You can also set the value of this cell using the **Snap** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="bccde-115">Pour obtenir une référence à la cellule Snap par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="bccde-115">To get a reference to the Snap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bccde-116">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="bccde-116">Cell name:</span></span>  <br/> |<span data-ttu-id="bccde-117">Layers. Snap [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bccde-117">Layers.Snap[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bccde-118">Pour obtenir une référence à la cellule Snap par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bccde-118">To get a reference to the Snap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bccde-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bccde-119">Section index:</span></span>  <br/> |<span data-ttu-id="bccde-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="bccde-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="bccde-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bccde-121">Row index:</span></span>  <br/> |<span data-ttu-id="bccde-122">**visRowLayer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bccde-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="bccde-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bccde-123">Cell index:</span></span>  <br/> |<span data-ttu-id="bccde-124">**visLayerSnap**</span><span class="sxs-lookup"><span data-stu-id="bccde-124">**visLayerSnap**</span></span> <br/> |
   

