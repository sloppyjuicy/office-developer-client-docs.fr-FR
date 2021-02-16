---
title: ShapePlowCode, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Détermine si cette forme positionnable se déplace lorsque vous placez une autre forme positionnable à côté d'elle sur la page de dessin.
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423894"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="8f1fe-103">ShapePlowCode, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="8f1fe-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="8f1fe-104">Détermine si cette forme positionnable se déplace lorsque vous placez une autre forme positionnable à côté d'elle sur la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="8f1fe-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8f1fe-105">**Value**</span></span>|<span data-ttu-id="8f1fe-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="8f1fe-106">**Description**</span></span>|<span data-ttu-id="8f1fe-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="8f1fe-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8f1fe-108">0</span><span class="sxs-lookup"><span data-stu-id="8f1fe-108">0</span></span>  <br/> |<span data-ttu-id="8f1fe-109">Tracer selon les paramètres de la page.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="8f1fe-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="8f1fe-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="8f1fe-111">1 </span><span class="sxs-lookup"><span data-stu-id="8f1fe-111">1</span></span>  <br/> |<span data-ttu-id="8f1fe-112">Ne tracer aucune forme.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="8f1fe-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="8f1fe-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="8f1fe-114">2 </span><span class="sxs-lookup"><span data-stu-id="8f1fe-114">2</span></span>  <br/> |<span data-ttu-id="8f1fe-115">Tracer chaque forme.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="8f1fe-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="8f1fe-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f1fe-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="8f1fe-117">Remarks</span></span>

<span data-ttu-id="8f1fe-118">Vous pouvez également définir la valeur de cette cellule pour  une forme particulière sous l’onglet [](run-in-developer-mode-display-the-developer-tab.md) **Placement** de  la boîte de dialogue Comportement (avec une forme sélectionnée, sous l’onglet Développeur, dans le groupe Création de formes, cliquez sur **Comportement,** puis cliquez sur l’onglet **Placement).**</span><span class="sxs-lookup"><span data-stu-id="8f1fe-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="8f1fe-119">Pour définir ce comportement pour  *toutes les formes*  de la page de dessin, utilisez la cellule PlowCode dans la section Mise en page.</span><span class="sxs-lookup"><span data-stu-id="8f1fe-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="8f1fe-120">Pour obtenir une référence à la cellule ShapePlowCode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="8f1fe-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f1fe-121">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8f1fe-121">Cell name:</span></span>  <br/> |<span data-ttu-id="8f1fe-122">ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="8f1fe-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="8f1fe-123">Pour obtenir une référence à la cellule ShapePlowCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8f1fe-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f1fe-124">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8f1fe-124">Section index:</span></span>  <br/> |<span data-ttu-id="8f1fe-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8f1fe-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8f1fe-126">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8f1fe-126">Row index:</span></span>  <br/> |<span data-ttu-id="8f1fe-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="8f1fe-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="8f1fe-128">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8f1fe-128">Cell index:</span></span>  <br/> |<span data-ttu-id="8f1fe-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="8f1fe-129">**visSLOPlowCode**</span></span> <br/> |
   

