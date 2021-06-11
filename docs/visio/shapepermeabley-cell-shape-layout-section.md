---
title: ShapePermeableY, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Détermine si un connecteur peut se positionner verticalement en traversant une forme positionnable.
ms.openlocfilehash: 62f8bfa0fdfb5c483836f344e8b784dc9092fded
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417517"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a><span data-ttu-id="7bff0-103">ShapePermeableY, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="7bff0-103">ShapePermeableY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="7bff0-104">Détermine si un connecteur peut se positionner verticalement en traversant une forme positionnable.</span><span class="sxs-lookup"><span data-stu-id="7bff0-104">Determines whether a connector can route vertically through a shape.</span></span>
  
|<span data-ttu-id="7bff0-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7bff0-105">**Value**</span></span>|<span data-ttu-id="7bff0-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="7bff0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7bff0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7bff0-107">TRUE</span></span>  <br/> |<span data-ttu-id="7bff0-108">Permet aux connecteurs de se positionner verticalement en traversant une forme positionnable.</span><span class="sxs-lookup"><span data-stu-id="7bff0-108">Enable connectors to route vertically through a shape.</span></span>  <br/> |
|<span data-ttu-id="7bff0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7bff0-109">FALSE</span></span>  <br/> |<span data-ttu-id="7bff0-110">Ne permet pas aux connecteurs de se positionner verticalement en traversant une forme positionnable.</span><span class="sxs-lookup"><span data-stu-id="7bff0-110">Do not let connectors route vertically through a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bff0-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="7bff0-111">Remarks</span></span>

<span data-ttu-id="7bff0-112">Vous pouvez également définir la valeur de cette  cellule sous l’onglet **Placement** dans la boîte  de dialogue Comportement (avec une forme sélectionnée, sous l’onglet Développeur, dans le groupe Création de formes, cliquez sur **Comportement,** puis cliquez sur l’onglet **Placement).** [](run-in-developer-mode-display-the-developer-tab.md)</span><span class="sxs-lookup"><span data-stu-id="7bff0-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="7bff0-113">Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="7bff0-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="7bff0-114">Pour obtenir une référence à la cellule ShapePermeableY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7bff0-114">To get a reference to the ShapePermeableY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7bff0-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7bff0-115">Cell name:</span></span>  <br/> |<span data-ttu-id="7bff0-116">ShapePermeableY</span><span class="sxs-lookup"><span data-stu-id="7bff0-116">ShapePermeableY</span></span>  <br/> |
   
<span data-ttu-id="7bff0-117">Pour obtenir une référence à la cellule ShapePermeableY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7bff0-117">To get a reference to the ShapePermeableY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7bff0-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7bff0-118">Section index:</span></span>  <br/> |<span data-ttu-id="7bff0-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7bff0-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7bff0-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7bff0-120">Row index:</span></span>  <br/> |<span data-ttu-id="7bff0-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="7bff0-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="7bff0-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7bff0-122">Cell index:</span></span>  <br/> |<span data-ttu-id="7bff0-123">**visSLOPermY**</span><span class="sxs-lookup"><span data-stu-id="7bff0-123">**visSLOPermY**</span></span> <br/> |
   

