---
title: CenterX, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60030
localization_priority: Normal
ms.assetid: 890e2537-66a5-2863-c78d-320b42565ea7
description: Détermine si la page de dessin est centrée horizontalement sur la page d'impression.
ms.openlocfilehash: a12b60f7d183a27d938bd18a1f571ef01af455d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788247"
---
# <a name="centerx-cell-print-properties-section"></a><span data-ttu-id="03b4b-103">CenterX, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="03b4b-103">CenterX Cell (Print Properties Section)</span></span>

<span data-ttu-id="03b4b-104">Détermine si la page de dessin est centrée horizontalement sur la page d'impression.</span><span class="sxs-lookup"><span data-stu-id="03b4b-104">Determines whether the drawing page is centered horizontally on the printer page.</span></span> 
  
|<span data-ttu-id="03b4b-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="03b4b-105">**Value**</span></span>|<span data-ttu-id="03b4b-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="03b4b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="03b4b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="03b4b-107">TRUE</span></span>  <br/> | <span data-ttu-id="03b4b-108">Centre la page de dessin horizontalement sur la page d'impression.</span><span class="sxs-lookup"><span data-stu-id="03b4b-108">Center the drawing page horizontally on the printer page.</span></span>  <br/> |
| <span data-ttu-id="03b4b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="03b4b-109">FALSE</span></span>  <br/> | <span data-ttu-id="03b4b-110">Ne centre pas la page de dessin horizontalement sur la page d'impression (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="03b4b-110">Do not center the drawing page horizontally on the printer page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03b4b-111">Note</span><span class="sxs-lookup"><span data-stu-id="03b4b-111">Remarks</span></span>

<span data-ttu-id="03b4b-p101">Par défaut, les pages de dessins sont alignées sur le haut et la gauche de la page d'impression. Définir les cellules CenterX et CenterY sur TRUE place la page de dessin au centre de la page d'impression (ou les pages lorsque la mosaïque est nécessaire).</span><span class="sxs-lookup"><span data-stu-id="03b4b-p101">By default, drawing pages are justified to the top and left of the printer page. Setting the CenterX and CenterY cells to TRUE places the drawing page in the center of the printer page (or pages when tiling is necessary).</span></span> 
  
<span data-ttu-id="03b4b-114">Pour obtenir une référence à la cellule CenterX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="03b4b-114">To get a reference to the CenterX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="03b4b-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="03b4b-115">Cell name:</span></span>  <br/> | <span data-ttu-id="03b4b-116">CenterX</span><span class="sxs-lookup"><span data-stu-id="03b4b-116">CenterX</span></span>  <br/> |
   
<span data-ttu-id="03b4b-117">Pour obtenir une référence à la cellule CenterX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="03b4b-117">To get a reference to the CenterX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="03b4b-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="03b4b-118">Section index:</span></span>  <br/> |<span data-ttu-id="03b4b-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="03b4b-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="03b4b-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="03b4b-120">Row index:</span></span>  <br/> |<span data-ttu-id="03b4b-121">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="03b4b-121">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="03b4b-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="03b4b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="03b4b-123">**visPrintPropertiesCenterX**</span><span class="sxs-lookup"><span data-stu-id="03b4b-123">**visPrintPropertiesCenterX**</span></span> <br/> |
   

