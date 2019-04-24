---
title: ShapePermeablePlace, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Détermine si des formes positionnables peuvent être placées sur une forme lors de la disposition des formes à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition).
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357056"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="dd5d4-103">ShapePermeablePlace, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="dd5d4-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="dd5d4-104">Détermine si des formes positionnables peuvent être placées sur une forme lors de la disposition des formes à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création**, dans le groupe **Disposition**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**).</span><span class="sxs-lookup"><span data-stu-id="dd5d4-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="dd5d4-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="dd5d4-105">**Value**</span></span>|<span data-ttu-id="dd5d4-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="dd5d4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd5d4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dd5d4-107">TRUE</span></span>  <br/> |<span data-ttu-id="dd5d4-108">Permet de placer les formes sur une forme.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="dd5d4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dd5d4-109">FALSE</span></span>  <br/> |<span data-ttu-id="dd5d4-110">Ne permet pas de placer les formes sur une forme.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd5d4-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd5d4-111">Remarks</span></span>

<span data-ttu-id="dd5d4-112">Vous pouvez également définir la valeur de cette cellule sous l'onglet **placement** de la boîte de dialogue **comportement** (sélectionnez une forme, sous l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe création de la **forme** , cliquez sur **comportement**, puis sur l'onglet **placement** . ).</span><span class="sxs-lookup"><span data-stu-id="dd5d4-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="dd5d4-113">Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="dd5d4-114">Pour obtenir une référence à la cellule ShapePermeablePlace par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="dd5d4-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd5d4-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dd5d4-115">Cell name:</span></span>  <br/> |<span data-ttu-id="dd5d4-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="dd5d4-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="dd5d4-117">Pour obtenir une référence à la cellule ShapePermeablePlace à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dd5d4-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd5d4-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="dd5d4-118">Section index:</span></span>  <br/> |<span data-ttu-id="dd5d4-119">**Définis**</span><span class="sxs-lookup"><span data-stu-id="dd5d4-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dd5d4-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="dd5d4-120">Row index:</span></span>  <br/> |<span data-ttu-id="dd5d4-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="dd5d4-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="dd5d4-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dd5d4-122">Cell index:</span></span>  <br/> |<span data-ttu-id="dd5d4-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="dd5d4-123">**visSLOPermeablePlace**</span></span> <br/> |
   

