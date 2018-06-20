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
description: Détermine si les formes positionnables peuvent être placées sur une forme lorsque des formes dans la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: 1873575eb4322d31f81c0dd34557c6167750ce82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789641"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="f8a46-103">ShapePermeablePlace, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="f8a46-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="f8a46-104">Détermine si les formes positionnables peuvent être placées sur une forme lorsque des formes dans la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur **autres Options de disposition **).</span><span class="sxs-lookup"><span data-stu-id="f8a46-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="f8a46-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f8a46-105">**Value**</span></span>|<span data-ttu-id="f8a46-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="f8a46-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8a46-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f8a46-107">TRUE</span></span>  <br/> |<span data-ttu-id="f8a46-108">Permet de placer les formes sur une forme.</span><span class="sxs-lookup"><span data-stu-id="f8a46-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="f8a46-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f8a46-109">FALSE</span></span>  <br/> |<span data-ttu-id="f8a46-110">Ne permet pas de placer les formes sur une forme.</span><span class="sxs-lookup"><span data-stu-id="f8a46-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8a46-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="f8a46-111">Remarks</span></span>

<span data-ttu-id="f8a46-112">Vous pouvez également définir la valeur de cette cellule dans l’onglet **Placement** dans la boîte de dialogue **comportement** (avec la forme sélectionnée, sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe **Création de la forme** , cliquez sur **comportement**, puis cliquez sur l’onglet **Placement** ).</span><span class="sxs-lookup"><span data-stu-id="f8a46-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="f8a46-113">Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="f8a46-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="f8a46-114">Pour obtenir une référence à la cellule ShapePermeablePlace par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="f8a46-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8a46-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f8a46-115">Cell name:</span></span>  <br/> |<span data-ttu-id="f8a46-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="f8a46-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="f8a46-117">Pour obtenir une référence à la cellule ShapePermeablePlace par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f8a46-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8a46-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f8a46-118">Section index:</span></span>  <br/> |<span data-ttu-id="f8a46-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f8a46-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f8a46-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f8a46-120">Row index:</span></span>  <br/> |<span data-ttu-id="f8a46-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="f8a46-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="f8a46-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f8a46-122">Cell index:</span></span>  <br/> |<span data-ttu-id="f8a46-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="f8a46-123">**visSLOPermeablePlace**</span></span> <br/> |
   

