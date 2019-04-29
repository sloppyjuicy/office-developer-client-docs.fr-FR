---
title: SortKey, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Nombre qui détermine l'ordre des liens hypertexte apparaissant dans un menu contextuel.
ms.openlocfilehash: 002ab036f5305aa6daa631c15b0e9eb6148a9635
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406380"
---
# <a name="sortkey-cell-hyperlinks-section"></a><span data-ttu-id="aeb35-103">SortKey, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="aeb35-103">SortKey Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="aeb35-104">Nombre qui détermine l'ordre des liens hypertexte apparaissant dans un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="aeb35-104">A number that determines the order of hyperlinks that appear on a shortcut menu.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aeb35-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="aeb35-105">Remarks</span></span>

<span data-ttu-id="aeb35-p101">Les liens hypertexte d'un menu contextuel apparaissent dans le menu dans l'ordre croissant, les numéros les plus petits figurant en haut du menu. Si deux lignes de lien hypertexte ont la même valeur de cellule SortKey, le classement est déterminé par l'ordre physique des lignes. La valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="aeb35-p101">The hyperlinks on a shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two hyperlink rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span> 
  
<span data-ttu-id="aeb35-109">Pour obtenir une référence à la cellule SortKey par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="aeb35-109">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aeb35-110">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="aeb35-110">Cell name:</span></span>  <br/> |<span data-ttu-id="aeb35-111">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="aeb35-111">Hyperlink.</span></span> <span data-ttu-id="aeb35-112">*nom* . SortKey où hyperLink *. nom* est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="aeb35-112">*name*  .SortKey where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="aeb35-113">Pour obtenir une référence à la cellule SortKey par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="aeb35-113">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aeb35-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="aeb35-114">Section index:</span></span>  <br/> |<span data-ttu-id="aeb35-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="aeb35-115">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="aeb35-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="aeb35-116">Row index:</span></span>  <br/> |<span data-ttu-id="aeb35-117">**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="aeb35-117">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="aeb35-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="aeb35-118">Cell index:</span></span>  <br/> |<span data-ttu-id="aeb35-119">**visHLinkSortKey**</span><span class="sxs-lookup"><span data-stu-id="aeb35-119">**visHLinkSortKey**</span></span> <br/> |
   

