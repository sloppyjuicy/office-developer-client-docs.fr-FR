---
title: CtrlAsInput, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Détermine la forme parente lors de la manipulation de formes avec des poignées de contrôle. Cette cellule définit le comportement de toutes les formes de la page de dessin.
ms.openlocfilehash: a530c48156043bec0cd58d79aead1a403c17ddce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422620"
---
# <a name="ctrlasinput-cell-page-layout-section"></a><span data-ttu-id="27ae8-104">CtrlAsInput, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="27ae8-104">CtrlAsInput Cell (Page Layout Section)</span></span>

<span data-ttu-id="27ae8-p102">Détermine la forme parente lors de la manipulation de formes avec des poignées de contrôle. Cette cellule définit le comportement de toutes les formes de la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="27ae8-p102">Determines which shape is the parent when using shapes with control handles. This cell sets the behavior for all the shapes on the drawing page.</span></span>
  
|<span data-ttu-id="27ae8-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="27ae8-107">**Value**</span></span>|<span data-ttu-id="27ae8-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="27ae8-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="27ae8-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="27ae8-109">TRUE</span></span>  <br/> | <span data-ttu-id="27ae8-110">Définit la forme à laquelle la poignée de contrôle est liée comme parent.</span><span class="sxs-lookup"><span data-stu-id="27ae8-110">Set the shape that the control handle is connected to as the parent.</span></span>  <br/> |
| <span data-ttu-id="27ae8-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="27ae8-111">FALSE</span></span>  <br/> | <span data-ttu-id="27ae8-p103">Valeur par défaut. Définit la forme contenant la poignée de contrôle comme parent.</span><span class="sxs-lookup"><span data-stu-id="27ae8-p103">The default. Set shape that contains the control handle as the parent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27ae8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="27ae8-114">Remarks</span></span>

<span data-ttu-id="27ae8-115">Pour obtenir une référence à la cellule CtrlAsInput par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="27ae8-115">To get a reference to the CtrlAsInput cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27ae8-116">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="27ae8-116">Cell name:</span></span>  <br/> | <span data-ttu-id="27ae8-117">CtrlAsInput</span><span class="sxs-lookup"><span data-stu-id="27ae8-117">CtrlAsInput</span></span>  <br/> |
   
<span data-ttu-id="27ae8-118">Pour obtenir une référence à la cellule CtrlAsInput à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="27ae8-118">To get a reference to the CtrlAsInput cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27ae8-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="27ae8-119">Section index:</span></span>  <br/> |<span data-ttu-id="27ae8-120">**Définis**</span><span class="sxs-lookup"><span data-stu-id="27ae8-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="27ae8-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="27ae8-121">Row index:</span></span>  <br/> |<span data-ttu-id="27ae8-122">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="27ae8-122">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="27ae8-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="27ae8-123">Cell index:</span></span>  <br/> |<span data-ttu-id="27ae8-124">**visPLOCtrlAsInput**</span><span class="sxs-lookup"><span data-stu-id="27ae8-124">**visPLOCtrlAsInput**</span></span> <br/> |
   

