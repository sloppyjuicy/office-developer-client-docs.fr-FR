---
title: QuickStyleVariation, cellule (Section Style rapide)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Détermine s’il faut remplacer les formules et les valeurs de texte, ligne et remplissage couleur (ou une combinaison de ces propriétés) à l’aide de couleurs qui contraste avec l’arrière-plan du diagramme. Valeur est une opération de bits OR de 0, 1, 2, 4 et 8.
ms.openlocfilehash: fe6462798b61a0713f98196974876144cf4606e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789386"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="f19cc-104">QuickStyleVariation, cellule (Section Style rapide)</span><span class="sxs-lookup"><span data-stu-id="f19cc-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="f19cc-105">Détermine s’il faut remplacer les formules et les valeurs de texte, ligne et remplissage couleur (ou une combinaison de ces propriétés) à l’aide de couleurs qui contraste avec l’arrière-plan du diagramme.</span><span class="sxs-lookup"><span data-stu-id="f19cc-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="f19cc-106">Valeur est une opération de bits OR de 0, 1, 2, 4 et 8.</span><span class="sxs-lookup"><span data-stu-id="f19cc-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="f19cc-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f19cc-107">**Value**</span></span>|<span data-ttu-id="f19cc-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="f19cc-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f19cc-109">0</span><span class="sxs-lookup"><span data-stu-id="f19cc-109">0</span></span>  <br/> |<span data-ttu-id="f19cc-110">Ne modifiez pas le texte d’une forme, ligne, ou remplissage couleur (ou n’importe quelle combinaison de ces propriétés) pour restent visibles par rapport à la couleur d’arrière-plan donnée d’un thème.</span><span class="sxs-lookup"><span data-stu-id="f19cc-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="f19cc-111">1</span><span class="sxs-lookup"><span data-stu-id="f19cc-111">1</span></span>  <br/> |<span data-ttu-id="f19cc-112">Ne modifiez pas le texte d’une forme, ligne, ou remplissage couleur (ou n’importe quelle combinaison de ces propriétés) pour restent visibles par rapport à la couleur d’arrière-plan donnée d’un thème.</span><span class="sxs-lookup"><span data-stu-id="f19cc-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="f19cc-113">2</span><span class="sxs-lookup"><span data-stu-id="f19cc-113">2</span></span>  <br/> |<span data-ttu-id="f19cc-114">Modifier la couleur du texte d’une forme, le cas échéant, reste visible par rapport à d’un thème couleur d’arrière-plan en fonction de le.</span><span class="sxs-lookup"><span data-stu-id="f19cc-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="f19cc-115">4</span><span class="sxs-lookup"><span data-stu-id="f19cc-115">4</span></span>  <br/> |<span data-ttu-id="f19cc-116">Modifier la couleur de trait d’une forme, si nécessaire, pour restent visibles auprès d’un thème donné la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f19cc-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="f19cc-117">8</span><span class="sxs-lookup"><span data-stu-id="f19cc-117">8</span></span>  <br/> |<span data-ttu-id="f19cc-118">Modifier la couleur de remplissage d’une forme, si nécessaire, pour restent visibles auprès d’un thème donné la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f19cc-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f19cc-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="f19cc-119">Remarks</span></span>

<span data-ttu-id="f19cc-120">Utilisez la cellule QuickStyleVariation afin de garantir la visibilité de texte ou de lignes lorsqu’elles se trouvent en dehors de toute la géométrie des formes visible (par exemple, dans une forme dont textbox est inférieure à la partie inférieure de la forme, telles que celles dans les diagrammes de réseau).</span><span class="sxs-lookup"><span data-stu-id="f19cc-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="f19cc-121">La valeur de cellule par défaut est 0, ce qui signifie que son comportement est inactif.</span><span class="sxs-lookup"><span data-stu-id="f19cc-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="f19cc-122">Toute autre valeur déclenche le comportement de la cellule.</span><span class="sxs-lookup"><span data-stu-id="f19cc-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="f19cc-123">La valeur QuickStyleVariation remplace la valeur générée par la fonction THEMEVAL lorsqu’il réside dans la couleur (Section caractère), FillForegnd ou LineColor cellules (ou générées par des références directes à ces trois propriétés prenait THEMEVAL ( » CharacterColor »), THEMEVAL("FillColor") et THEMEVAL("LineColor")).</span><span class="sxs-lookup"><span data-stu-id="f19cc-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="f19cc-124">Pour obtenir une référence à la cellule **QuickStyleVariation** par un nom à partir d’une autre formule, en obtenant la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="f19cc-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f19cc-125">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f19cc-125">Cell name:</span></span>  <br/> |<span data-ttu-id="f19cc-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="f19cc-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="f19cc-127">Pour obtenir une référence à la cellule **QuickStyleVariation** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f19cc-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f19cc-128">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f19cc-128">Section index:</span></span>  <br/> |<span data-ttu-id="f19cc-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f19cc-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f19cc-130">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f19cc-130">Row index:</span></span>  <br/> |<span data-ttu-id="f19cc-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="f19cc-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="f19cc-132">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f19cc-132">Cell index:</span></span>  <br/> |<span data-ttu-id="f19cc-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="f19cc-133">**visQuickStyleVariation**</span></span> <br/> |
   

