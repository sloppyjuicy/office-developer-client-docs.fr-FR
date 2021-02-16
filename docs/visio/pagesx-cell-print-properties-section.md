---
title: PagesX, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60064
localization_priority: Normal
ms.assetid: a10bf4c2-24f4-4c53-39ba-2b8cd5b50d2c
description: Détermine le nombre de pages d'impression sur lesquelles ajuster la page de dessin horizontalement.
ms.openlocfilehash: e912aef2277f5a7d2af5352897654ee986836c48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438693"
---
# <a name="pagesx-cell-print-properties-section"></a><span data-ttu-id="ba1df-103">PagesX, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="ba1df-103">PagesX Cell (Print Properties Section)</span></span>

<span data-ttu-id="ba1df-104">Détermine le nombre de pages d'impression sur lesquelles ajuster la page de dessin horizontalement.</span><span class="sxs-lookup"><span data-stu-id="ba1df-104">Determines the number of printer pages on which to fit the drawing page horizontally.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ba1df-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="ba1df-105">Remarks</span></span>

<span data-ttu-id="ba1df-106">Cette valeur n'est utilisée que lorsque la cellule OnPage est définie sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="ba1df-106">This value is used only when the OnPage cell is set to TRUE.</span></span> 
  
<span data-ttu-id="ba1df-107">Pour obtenir une référence à la cellule PagesX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ba1df-107">To get a reference to the PagesX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ba1df-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ba1df-108">Cell name:</span></span>  <br/> | <span data-ttu-id="ba1df-109">PagesX</span><span class="sxs-lookup"><span data-stu-id="ba1df-109">PagesX</span></span>  <br/> |
   
<span data-ttu-id="ba1df-110">Pour obtenir une référence à la cellule PagesX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ba1df-110">To get a reference to the PagesX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ba1df-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ba1df-111">Section index:</span></span>  <br/> |<span data-ttu-id="ba1df-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ba1df-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ba1df-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ba1df-113">Row index:</span></span>  <br/> |<span data-ttu-id="ba1df-114">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="ba1df-114">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="ba1df-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ba1df-115">Cell index:</span></span>  <br/> |<span data-ttu-id="ba1df-116">**visPrintPropertiesPagesX**</span><span class="sxs-lookup"><span data-stu-id="ba1df-116">**visPrintPropertiesPagesX**</span></span> <br/> |
   

