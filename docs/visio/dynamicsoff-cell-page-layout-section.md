---
title: DynamicsOff, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: Détermine si les formes positionnables se déplacent et si les connecteurs sont repositionnés autour des autres formes et des connecteurs sur la page de dessin.
ms.openlocfilehash: 72d65860d1a2ee37efd5287ae3f4baf54bd3addb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788534"
---
# <a name="dynamicsoff-cell-page-layout-section"></a><span data-ttu-id="496f4-103">DynamicsOff, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="496f4-103">DynamicsOff Cell (Page Layout Section)</span></span>

<span data-ttu-id="496f4-104">Détermine si les formes positionnables se déplacent et si les connecteurs sont repositionnés autour des autres formes et des connecteurs sur la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="496f4-104">Determines whether placeable shapes move and connectors reroute around other shapes and connectors on the drawing page.</span></span>
  
|<span data-ttu-id="496f4-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="496f4-105">**Value**</span></span>|<span data-ttu-id="496f4-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="496f4-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="496f4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="496f4-107">TRUE</span></span>  <br/> | <span data-ttu-id="496f4-108">Désactive le repositionnement automatique.</span><span class="sxs-lookup"><span data-stu-id="496f4-108">Disable dynamics.</span></span>  <br/> |
| <span data-ttu-id="496f4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="496f4-109">FALSE</span></span>  <br/> | <span data-ttu-id="496f4-110">Active le repositionnement automatique.</span><span class="sxs-lookup"><span data-stu-id="496f4-110">Enable dynamics.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="496f4-111">Note</span><span class="sxs-lookup"><span data-stu-id="496f4-111">Remarks</span></span>

<span data-ttu-id="496f4-p101">Vous pouvez désactiver le repositionnement automatique pour augmenter les performances de votre solution. Par exemple, si votre solution ajoute des formes positionnables sur un dessin et si vous ne souhaitez pas que l'application repositionne les connecteurs et les formes chaque fois que vous ajoutez une forme, vous pouvez désactiver cette fonction, puis la réactiver après que votre solution a fini d'ajouter des formes.</span><span class="sxs-lookup"><span data-stu-id="496f4-p101">You can disable dynamics to increase your solution's performance. For example, if your solution adds placeable shapes to a drawing and you don't want the application to reroute connectors and reposition shapes each time you add a shape, you can disable dynamics. After your solution adds the shapes, re-enable dynamics.</span></span>
  
<span data-ttu-id="496f4-115">Pour obtenir une référence à la cellule DynamcOff par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="496f4-115">To get a reference to the DynamicsOff cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="496f4-116">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="496f4-116">Cell name:</span></span>  <br/> | <span data-ttu-id="496f4-117">DynamicsOff</span><span class="sxs-lookup"><span data-stu-id="496f4-117">DynamicsOff</span></span>  <br/> |
   
<span data-ttu-id="496f4-118">Pour obtenir une référence à la cellule DynamcOff par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="496f4-118">To get a reference to the DynamicsOff cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="496f4-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="496f4-119">Section index:</span></span>  <br/> |<span data-ttu-id="496f4-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="496f4-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="496f4-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="496f4-121">Row index:</span></span>  <br/> |<span data-ttu-id="496f4-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="496f4-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="496f4-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="496f4-123">Cell index:</span></span>  <br/> |<span data-ttu-id="496f4-124">**visPLODynamicsOff**</span><span class="sxs-lookup"><span data-stu-id="496f4-124">**visPLODynamicsOff**</span></span> <br/> |
   

