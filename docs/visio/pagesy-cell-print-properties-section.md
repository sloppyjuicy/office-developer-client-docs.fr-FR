---
title: PagesY, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
localization_priority: Normal
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Détermine le nombre de pages d'impression sur lesquelles ajuster verticalement la page de dessin.
ms.openlocfilehash: 43d4081439525c516d3da28b6c0e46e9273d85c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429781"
---
# <a name="pagesy-cell-print-properties-section"></a><span data-ttu-id="79773-103">PagesY, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="79773-103">PagesY Cell (Print Properties Section)</span></span>

<span data-ttu-id="79773-104">Détermine le nombre de pages d'impression sur lesquelles ajuster verticalement la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="79773-104">Determines the number of printer pages on which to fit the drawing page vertically.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="79773-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="79773-105">Remarks</span></span>

<span data-ttu-id="79773-106">Cette valeur n'est utilisée que lorsque la cellule OnPage est définie sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="79773-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="79773-107">Pour obtenir une référence à la cellule PagesY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="79773-107">To get a reference to the PagesY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="79773-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="79773-108">Cell name:</span></span>  <br/> | <span data-ttu-id="79773-109">PagesY</span><span class="sxs-lookup"><span data-stu-id="79773-109">PagesY</span></span>  <br/> |
   
<span data-ttu-id="79773-110">Pour obtenir une référence à la cellule PagesY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="79773-110">To get a reference to the PagesY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="79773-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="79773-111">Section index:</span></span>  <br/> |<span data-ttu-id="79773-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="79773-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="79773-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="79773-113">Row index:</span></span>  <br/> |<span data-ttu-id="79773-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="79773-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="79773-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="79773-115">Cell index:</span></span>  <br/> |<span data-ttu-id="79773-116">**visPrintPropertiesPagesY**</span><span class="sxs-lookup"><span data-stu-id="79773-116">**visPrintPropertiesPagesY**</span></span> <br/> |
   

