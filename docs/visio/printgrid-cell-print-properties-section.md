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
ms.openlocfilehash: 9b98999cd02fa6a47ec8564bbd7337ecf8637306
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315189"
---
# <a name="printgrid-cell-print-properties-section"></a><span data-ttu-id="8a49d-103">PrintGrid, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="8a49d-103">PrintGrid Cell (Print Properties Section)</span></span>

<span data-ttu-id="8a49d-104">Indique si la grille sera imprimée lors de l'impression d'une page de document.</span><span class="sxs-lookup"><span data-stu-id="8a49d-104">Specifies whether to print the grid when printing a document page.</span></span>
  
|<span data-ttu-id="8a49d-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="8a49d-105">**Value**</span></span>|<span data-ttu-id="8a49d-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a49d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a49d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8a49d-107">TRUE</span></span>  <br/> |<span data-ttu-id="8a49d-108">Affiche la grille lors de l'impression de cette page.</span><span class="sxs-lookup"><span data-stu-id="8a49d-108">Show the grid when printing this page.</span></span>  <br/> |
|<span data-ttu-id="8a49d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8a49d-109">FALSE</span></span>  <br/> |<span data-ttu-id="8a49d-110">N'affiche pas la grille lors de l'impression de cette page (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="8a49d-110">Do not show the grid when printing this page (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a49d-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a49d-111">Remarks</span></span>

<span data-ttu-id="8a49d-p101">Cette valeur correspond à la case à cocher **Quadrillage** sous l’onglet **Configuration** de la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur **Mise en page**). Exception faite de la couleur (la version imprimée est grise), la grille imprimée est identique à celle que vous voyez dans la fenêtre de dessin Microsoft Office Visio.</span><span class="sxs-lookup"><span data-stu-id="8a49d-p101">This value corresponds to the **Gridlines** check box on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). Other than color (the printed version is gray), the printed grid is identical to the grid you see in the Microsoft Visio drawing window.</span></span> 
  
<span data-ttu-id="8a49d-114">Vous pouvez choisir d’imprimer la grille page par page.</span><span class="sxs-lookup"><span data-stu-id="8a49d-114">You can choose whether to print the grid on a page-by-page basis.</span></span> <span data-ttu-id="8a49d-115">Le style de grille peut également être défini page par page dans la boîte de dialogue grille de \*\*règle &amp; \*\* (sous l'onglet **affichage** , cliquez sur la flèche **Afficher** ) lorsqu'une page est active.</span><span class="sxs-lookup"><span data-stu-id="8a49d-115">The style of grid can also be defined on a page-by-page basis in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow) when a page is active.</span></span> 
  
<span data-ttu-id="8a49d-116">Pour obtenir une référence à la cellule PrintGrid par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="8a49d-116">To get a reference to the PrintGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a49d-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8a49d-117">Cell name:</span></span>  <br/> |<span data-ttu-id="8a49d-118">PrintGrid</span><span class="sxs-lookup"><span data-stu-id="8a49d-118">PrintGrid</span></span>  <br/> |
   
<span data-ttu-id="8a49d-119">Pour obtenir une référence à la cellule PrintGrid à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8a49d-119">To get a reference to the PrintGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a49d-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8a49d-120">Section index:</span></span>  <br/> |<span data-ttu-id="8a49d-121">**Définis**</span><span class="sxs-lookup"><span data-stu-id="8a49d-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8a49d-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8a49d-122">Row index:</span></span>  <br/> |<span data-ttu-id="8a49d-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="8a49d-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="8a49d-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8a49d-124">Cell index:</span></span>  <br/> |<span data-ttu-id="8a49d-125">**visPrintPropertiesPrintGrid**</span><span class="sxs-lookup"><span data-stu-id="8a49d-125">**visPrintPropertiesPrintGrid**</span></span> <br/> |
   

