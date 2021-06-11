---
title: À propos de la fenêtre Suivi des formules
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
localization_priority: Normal
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: La fenêtre Suivi des formules est conçue pour fournir aux développeurs de formes des informations à propos d’interdépendances entre des cellules — à la fois des cellules dépendantes (qui dépendent d’une cellule en particulier) et des cellules précédentes (dont dépend une cellule en particulier).
ms.openlocfilehash: f5f9d6a7ba3ab7049715d31342cfe7aa68ea053f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345315"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="9cb43-103">À propos de la fenêtre Suivi des formules</span><span class="sxs-lookup"><span data-stu-id="9cb43-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="9cb43-104">La fenêtre **Suivi des formules** est conçue pour fournir aux développeurs de formes des informations à propos d’interdépendances entre des cellules — à la fois des cellules dépendantes (qui dépendent d’une cellule en particulier) et des cellules précédentes (dont dépend une cellule en particulier).</span><span class="sxs-lookup"><span data-stu-id="9cb43-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="9cb43-105">Les cellules d’une feuille ShapeSheet Microsoft Visio contiennent des valeurs et des formules.</span><span class="sxs-lookup"><span data-stu-id="9cb43-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="9cb43-106">Les formules peuvent, à leur tour, avoir des références à d’autres cellules, ce qui vous donne la puissance de calculer une valeur dans une cellule en fonction de la valeur d’une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="9cb43-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="9cb43-107">Toutefois, en créant ou en maintenant des formes complexes, il peut s’avérer difficile d’identifier toutes ces interdépendances car une formule peut faire référence à n’importe quelle cellule du dessin, qu’il s’agisse d’une cellule de la même feuille ShapeSheet ou d’une cellule appartenant à un autre objet du dessin comme une page, un style, une forme de base ou une autre forme.</span><span class="sxs-lookup"><span data-stu-id="9cb43-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="9cb43-108">La **fenêtre Suivi des** formules fournit des informations pour vous aider à comprendre les implications des modifications apportées aux cellules.</span><span class="sxs-lookup"><span data-stu-id="9cb43-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="9cb43-109">Affichage de la fenêtre Suivi des formules</span><span class="sxs-lookup"><span data-stu-id="9cb43-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="9cb43-110">Pour afficher  la fenêtre Suivi des formules, avec la fenêtre Feuille ShapeSheet active,  sous Outils **Feuille ShapeSheet** sous l’onglet \*\* Création \*\*, dans le groupe Suivi des formules, cliquez sur **Afficher la fenêtre.**</span><span class="sxs-lookup"><span data-stu-id="9cb43-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="9cb43-111">La  fenêtre Suivi des formules apparaît ancrée dans la fenêtre Feuille ShapeSheet par défaut, mais il s’agit d’une fenêtre ancrée qui peut être ancrée, flottante ou fusionnée avec d’autres fenêtres ShapeSheet ancrées disponibles, par exemple la fenêtre Explorateur de **styles.**</span><span class="sxs-lookup"><span data-stu-id="9cb43-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="9cb43-112">Cellules Tracing dependent</span><span class="sxs-lookup"><span data-stu-id="9cb43-112">Tracing dependent cells</span></span>

<span data-ttu-id="9cb43-p103">Pour une liste des cellules dépendantes d’une cellule en particulier, sélectionnez cette cellule dans la fenêtre ShapeSheet. Dans cet exemple, la cellule Width est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9cb43-p103">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window. In this example, the Width cell is selected.</span></span> 
  
![La cellule Width est sélectionnée](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="9cb43-116">Pour afficher ses cellules dépendantes, dans le groupe **Suivi** des **formules, cliquez sur Dépendants du suivi.**</span><span class="sxs-lookup"><span data-stu-id="9cb43-116">To view its dependent cells, in the **Formula Tracing** group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="9cb43-p104">Une liste reprenant toutes les cellules dépendantes de la cellule Width apparaît dans la fenêtre **Suivi des formules**. Vous pouvez accéder à n’importe quelle cellule de la liste en double-cliquant sur son entrée dans la fenêtre **Suivi des formules**.</span><span class="sxs-lookup"><span data-stu-id="9cb43-p104">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window. You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Toutes les cellules ayant une dépendance sur la cellule Width apparaissent dans la fenêtre Suivi des formules](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="9cb43-120">Cellules pré-cendentes de suivi</span><span class="sxs-lookup"><span data-stu-id="9cb43-120">Tracing precendent cells</span></span>

<span data-ttu-id="9cb43-p105">Pour une liste des cellules dont une cellule en particulier est dépendante, sélectionnez d’abord la cellule dans la fenêtre ShapeSheet. Dans cet exemple, Ia cellule Geometry1.X2 est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9cb43-p105">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window. In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![La cellule Geometry1.X2 est sélectionnée](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="9cb43-124">Pour afficher ses cellules précédentes, dans le groupe **Suivi** des formules, cliquez **sur Suivi des antécédents.**</span><span class="sxs-lookup"><span data-stu-id="9cb43-124">To view its precedent cells, in the **Formula Tracing** group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="9cb43-125">La liste de toutes les cellules dont dépend la cellule Geometry1.X2 apparaît dans la fenêtre Suivi **des** formules.</span><span class="sxs-lookup"><span data-stu-id="9cb43-125">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="9cb43-126">Vous pouvez accéder à n’importe quelle cellule de la liste en double-cliquant sur son entrée dans la fenêtre **Suivi des formules**.</span><span class="sxs-lookup"><span data-stu-id="9cb43-126">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Toutes les cellules dont dépend la cellule Geometry1.X2 apparaissent dans la fenêtre Suivi des formules](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

