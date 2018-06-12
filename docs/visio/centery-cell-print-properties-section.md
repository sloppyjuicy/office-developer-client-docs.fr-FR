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
ms.openlocfilehash: 2fde1d6301d7b9de4540cd12f21e5af01d7a6239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788266"
---
# <a name="centery-cell-print-properties-section"></a><span data-ttu-id="18a46-103">CenterY, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="18a46-103">CenterY Cell (Print Properties Section)</span></span>

<span data-ttu-id="18a46-104">Détermine si la page de dessin est centrée verticalement sur la page d'impression.</span><span class="sxs-lookup"><span data-stu-id="18a46-104">Determines whether the drawing page is centered vertically on the printer page.</span></span> 
  
|<span data-ttu-id="18a46-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="18a46-105">**Value**</span></span>|<span data-ttu-id="18a46-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="18a46-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="18a46-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="18a46-107">TRUE</span></span>  <br/> | <span data-ttu-id="18a46-108">Centre la page de dessin verticalement sur la page d'impression.</span><span class="sxs-lookup"><span data-stu-id="18a46-108">Center the drawing page vertically on the printer page.</span></span>  <br/> |
| <span data-ttu-id="18a46-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="18a46-109">FALSE</span></span>  <br/> | <span data-ttu-id="18a46-110">Ne centre pas la page de dessin verticalement sur la page d'impression (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="18a46-110">Do not center the drawing page vertically on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18a46-111">Note</span><span class="sxs-lookup"><span data-stu-id="18a46-111">Remarks</span></span>

<span data-ttu-id="18a46-p101">Par défaut, les pages de dessins sont alignées sur le haut et la gauche de la page d'impression. Définir les cellules CenterX et CenterY sur TRUE place la page de dessin au centre de la page d'impression (ou les pages lorsque la mosaïque est nécessaire).</span><span class="sxs-lookup"><span data-stu-id="18a46-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="18a46-114">Pour obtenir une référence à la cellule CenterY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="18a46-114">To get a reference to the CenterY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18a46-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="18a46-115">Cell name:</span></span>  <br/> | <span data-ttu-id="18a46-116">CenterY</span><span class="sxs-lookup"><span data-stu-id="18a46-116">CenterY</span></span>  <br/> |
   
<span data-ttu-id="18a46-117">Pour obtenir une référence à la cellule CenterY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="18a46-117">To get a reference to the CenterY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18a46-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="18a46-118">Section index:</span></span>  <br/> |<span data-ttu-id="18a46-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="18a46-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="18a46-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="18a46-120">Row index:</span></span>  <br/> |<span data-ttu-id="18a46-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="18a46-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="18a46-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="18a46-122">Cell index:</span></span>  <br/> |<span data-ttu-id="18a46-123">**visPrintPropertiesCenterY**</span><span class="sxs-lookup"><span data-stu-id="18a46-123">**visPrintPropertiesCenterY**</span></span> <br/> |
   

