---
title: QuickStyleVariation Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Détermine s'il faut remplacer les formules et les valeurs de texte, de trait et de couleur de remplissage (ou une combinaison de ces propriétés) à l'aide de couleurs qui contrastent avec l'arrière-plan du diagramme. La valeur est un opérateur de bits or de 0, 1, 2, 4 et 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360013"
---
# <a name="quickstylevariation-cell-quick-style-section"></a><span data-ttu-id="01f06-104">QuickStyleVariation Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="01f06-104">QuickStyleVariation Cell (Quick Style Section)</span></span>

<span data-ttu-id="01f06-105">Détermine s'il faut remplacer les formules et les valeurs de texte, de trait et de couleur de remplissage (ou une combinaison de ces propriétés) à l'aide de couleurs qui contrastent avec l'arrière-plan du diagramme.</span><span class="sxs-lookup"><span data-stu-id="01f06-105">Determines whether to override the formulas and values of text, line, and fill color (or a combination of those properties) by using colors that contrast with the diagram background.</span></span> <span data-ttu-id="01f06-106">La valeur est un opérateur de bits or de 0, 1, 2, 4 et 8.</span><span class="sxs-lookup"><span data-stu-id="01f06-106">Value is a bitwise OR of 0, 1, 2, 4, and 8.</span></span>
  
|<span data-ttu-id="01f06-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="01f06-107">**Value**</span></span>|<span data-ttu-id="01f06-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="01f06-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="01f06-109">0</span><span class="sxs-lookup"><span data-stu-id="01f06-109">0</span></span>  <br/> |<span data-ttu-id="01f06-110">Ne modifiez pas le texte, la ligne ou la couleur de remplissage d'une forme (ou n'importe quelle combinaison de ces propriétés) pour qu'elle reste visible par rapport à la couleur d'arrière-plan d'un thème.</span><span class="sxs-lookup"><span data-stu-id="01f06-110">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="01f06-111">0,1</span><span class="sxs-lookup"><span data-stu-id="01f06-111">1</span></span>  <br/> |<span data-ttu-id="01f06-112">Ne modifiez pas le texte, la ligne ou la couleur de remplissage d'une forme (ou n'importe quelle combinaison de ces propriétés) pour qu'elle reste visible par rapport à la couleur d'arrière-plan d'un thème.</span><span class="sxs-lookup"><span data-stu-id="01f06-112">Do not alter a shape's text, line, or fill color (or any combination of those properties) to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="01f06-113">n°2</span><span class="sxs-lookup"><span data-stu-id="01f06-113">2</span></span>  <br/> |<span data-ttu-id="01f06-114">Modifier la couleur du texte d'une forme, si nécessaire, pour rester visible par rapport à la couleur d'arrière-plan d'un thème donnée.</span><span class="sxs-lookup"><span data-stu-id="01f06-114">Alter a shape's text color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="01f06-115">4</span><span class="sxs-lookup"><span data-stu-id="01f06-115">4</span></span>  <br/> |<span data-ttu-id="01f06-116">Modifier la couleur de trait d'une forme, si nécessaire, pour rester visible par rapport à la couleur d'arrière-plan d'un thème donnée.</span><span class="sxs-lookup"><span data-stu-id="01f06-116">Alter a shape's line color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
|<span data-ttu-id="01f06-117">8bits</span><span class="sxs-lookup"><span data-stu-id="01f06-117">8</span></span>  <br/> |<span data-ttu-id="01f06-118">Modifier la couleur de remplissage d'une forme, si nécessaire, pour rester visible par rapport à la couleur d'arrière-plan d'un thème donnée.</span><span class="sxs-lookup"><span data-stu-id="01f06-118">Alter a shape's fill color, if necessary, to remain visible against a theme's given background color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01f06-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="01f06-119">Remarks</span></span>

<span data-ttu-id="01f06-120">Utilisez la cellule QuickStyleVariation pour garantir une visibilité en texte ou en lignes lorsqu'elles se trouvent en dehors de toute géométrie de forme visible (par exemple, dans une forme dont la zone de texte se trouve en dessous du bas de la forme, comme celles des diagrammes de réseaux).</span><span class="sxs-lookup"><span data-stu-id="01f06-120">Use the QuickStyleVariation cell to guarantee visibility in either text or lines when they are outside any visible shape geometry (for example, in a shape whose textbox is below the bottom of the shape, such as those in Network Diagrams).</span></span> <span data-ttu-id="01f06-121">La valeur par défaut de la cellule est 0, ce qui signifie que son comportement est inactif.</span><span class="sxs-lookup"><span data-stu-id="01f06-121">The cell's default value is 0, which means that its behavior is inactive.</span></span> <span data-ttu-id="01f06-122">Toute autre valeur déclenche le comportement de la cellule.</span><span class="sxs-lookup"><span data-stu-id="01f06-122">Any other value triggers the cell's behavior.</span></span>
  
<span data-ttu-id="01f06-123">La valeur QuickStyleVariation remplace la valeur produite par la fonction THEMEVAL lorsqu'elle réside dans les cellules Color (section Character), FillForegnd ou LineColor (ou produites par des références directes à ces trois propriétés par le biais de THEMEVAL (" CharacterColor "), THEMEVAL (" FillColor ") et THEMEVAL (" LineColor ")).</span><span class="sxs-lookup"><span data-stu-id="01f06-123">The QuickStyleVariation value overrides the value produced by the THEMEVAL function when it resides in the Color (Character Section), FillForegnd, or LineColor cells (or produced by direct references to these three properties by means of THEMEVAL("CharacterColor"), THEMEVAL("FillColor"), and THEMEVAL("LineColor")).</span></span>
  
<span data-ttu-id="01f06-124">Pour obtenir une référence à la cellule **QuickStyleVariation** par un nom à partir d'une autre formule, en obtenant la valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="01f06-124">To get a reference to the **QuickStyleVariation** cell by name from another formula, by getting the value of the **N** attribute of a **Cell** element, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f06-125">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="01f06-125">Cell name:</span></span>  <br/> |<span data-ttu-id="01f06-126">QuickStyleVariation</span><span class="sxs-lookup"><span data-stu-id="01f06-126">QuickStyleVariation</span></span>  <br/> |
   
<span data-ttu-id="01f06-127">Pour obtenir une référence à la cellule **QuickStyleVariation** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="01f06-127">To get a reference to the **QuickStyleVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f06-128">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="01f06-128">Section index:</span></span>  <br/> |<span data-ttu-id="01f06-129">**Définis**</span><span class="sxs-lookup"><span data-stu-id="01f06-129">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="01f06-130">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="01f06-130">Row index:</span></span>  <br/> |<span data-ttu-id="01f06-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="01f06-131">**visRowQuickStyleProperties**</span></span> <br/> |
|<span data-ttu-id="01f06-132">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="01f06-132">Cell index:</span></span>  <br/> |<span data-ttu-id="01f06-133">**visQuickStyleVariation**</span><span class="sxs-lookup"><span data-stu-id="01f06-133">**visQuickStyleVariation**</span></span> <br/> |
   

