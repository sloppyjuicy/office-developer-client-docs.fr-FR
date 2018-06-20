---
title: PrintGrid, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Indique si la grille sera imprimée lors de l'impression d'une page de document.
ms.openlocfilehash: 76e5b5b4e82c39cbbffbecc710f05a77dbaa6332
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789371"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="83ffc-103">PrintGrid, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="83ffc-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="83ffc-104">Indique si la grille sera imprimée lors de l'impression d'une page de document.</span><span class="sxs-lookup"><span data-stu-id="83ffc-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="83ffc-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="83ffc-105">**Value**</span></span>|<span data-ttu-id="83ffc-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="83ffc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="83ffc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="83ffc-107">TRUE</span></span>  <br/> |<span data-ttu-id="83ffc-108">Affiche la grille lors de l'impression de cette page.</span><span class="sxs-lookup"><span data-stu-id="83ffc-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="83ffc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="83ffc-109">FALSE</span></span>  <br/> |<span data-ttu-id="83ffc-110">N'affiche pas la grille lors de l'impression de cette page (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="83ffc-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83ffc-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="83ffc-111">Remarks</span></span>

<span data-ttu-id="83ffc-112">Cette valeur correspond à la case à cocher **quadrillage** sous l’onglet **Configuration de l’impression** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ).</span><span class="sxs-lookup"><span data-stu-id="83ffc-112">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="83ffc-113">Autre couleur (la version imprimée est grise), la grille imprimée est identique à la grille s’affiche dans la fenêtre de dessin Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="83ffc-113">Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="83ffc-114">Vous pouvez choisir s’il faut imprimer la grille sur une base de page par page.</span><span class="sxs-lookup"><span data-stu-id="83ffc-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="83ffc-115">Le style de grille peut également être défini sur une base de page par page dans la **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ) lorsqu’une page est active.</span><span class="sxs-lookup"><span data-stu-id="83ffc-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="83ffc-116">Pour obtenir une référence à la cellule PrintGrid par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="83ffc-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="83ffc-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="83ffc-117">Cell name:</span></span>  <br/> |<span data-ttu-id="83ffc-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="83ffc-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="83ffc-119">Pour obtenir une référence à la cellule PrintGrid par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="83ffc-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="83ffc-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="83ffc-120">Section index:</span></span>  <br/> |<span data-ttu-id="83ffc-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="83ffc-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="83ffc-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="83ffc-122">Row index:</span></span>  <br/> |<span data-ttu-id="83ffc-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="83ffc-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="83ffc-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="83ffc-124">Cell index:</span></span>  <br/> |<span data-ttu-id="83ffc-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="83ffc-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

