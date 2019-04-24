---
title: CenterY, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033792
localization_priority: Normal
ms.assetid: 7ce0bf66-dc8b-9646-7b04-50c969ecd67a
description: Détermine si la page de dessin est centrée verticalement sur la page d'impression.
ms.openlocfilehash: 858bf41c74fdcbd82d271a379df7c5816a7796fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341915"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="3fef3-103">CenterY, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="3fef3-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="3fef3-104">Détermine si la page de dessin est centrée verticalement sur la page d'impression.</span><span class="sxs-lookup"><span data-stu-id="3fef3-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="3fef3-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="3fef3-105">**Value**</span></span>|<span data-ttu-id="3fef3-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="3fef3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3fef3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3fef3-107">TRUE</span></span>  <br/> | <span data-ttu-id="3fef3-108">Centre la page de dessin verticalement sur la page d'impression.</span><span class="sxs-lookup"><span data-stu-id="3fef3-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="3fef3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3fef3-109">FALSE</span></span>  <br/> | <span data-ttu-id="3fef3-110">Ne centre pas la page de dessin verticalement sur la page d'impression (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="3fef3-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fef3-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="3fef3-111">Remarks</span></span>

<span data-ttu-id="3fef3-p101">Par défaut, les pages de dessins sont alignées sur le haut et la gauche de la page d'impression. Définir les cellules CenterX et CenterY sur TRUE place la page de dessin au centre de la page d'impression (ou les pages lorsque la mosaïque est nécessaire).</span><span class="sxs-lookup"><span data-stu-id="3fef3-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="3fef3-114">Pour obtenir une référence à la cellule CenterY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="3fef3-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3fef3-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3fef3-115">Cell name:</span></span>  <br/> | <span data-ttu-id="3fef3-116">CenterY</span><span class="sxs-lookup"><span data-stu-id="3fef3-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="3fef3-117">Pour obtenir une référence à la cellule CenterY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3fef3-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3fef3-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="3fef3-118">Section index:</span></span>  <br/> |<span data-ttu-id="3fef3-119">**Définis**</span><span class="sxs-lookup"><span data-stu-id="3fef3-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3fef3-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="3fef3-120">Row index:</span></span>  <br/> |<span data-ttu-id="3fef3-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="3fef3-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="3fef3-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3fef3-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3fef3-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="3fef3-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   

