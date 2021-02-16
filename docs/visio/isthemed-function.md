---
title: Fonction ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Cette propriété renvoie une valeur de booléen indiquant si un thème est appliqué à une forme.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418119"
---
# <a name="isthemed-function"></a><span data-ttu-id="881f2-103">Fonction ISTHEMED</span><span class="sxs-lookup"><span data-stu-id="881f2-103">ISTHEMED Function</span></span>

<span data-ttu-id="881f2-104">Cette propriété renvoie une valeur de booléen indiquant si un thème est appliqué à une forme.</span><span class="sxs-lookup"><span data-stu-id="881f2-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="881f2-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="881f2-105">Version Information</span></span>

<span data-ttu-id="881f2-106">Version ajoutée : Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="881f2-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="881f2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="881f2-107">Syntax</span></span>

 <span data-ttu-id="881f2-108">**ISTHEMED**()</span><span class="sxs-lookup"><span data-stu-id="881f2-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="881f2-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="881f2-109">Return value</span></span>

<span data-ttu-id="881f2-110">Booléen</span><span class="sxs-lookup"><span data-stu-id="881f2-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="881f2-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="881f2-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="881f2-112">La **fonction ISTHEMED** dans Visio 2013 remplace la fonction **CELLISTHEMED** des versions précédentes de Visio.</span><span class="sxs-lookup"><span data-stu-id="881f2-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="881f2-113">La **fonction ISTHEMED** vous permet d’affecter des parties appropriées de la mise en forme d’un thème à une forme, tout en conservant la possibilité de remplacer d’autres parties de la mise en forme de thème par une mise en forme appliquée manuellement.</span><span class="sxs-lookup"><span data-stu-id="881f2-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="881f2-114">Si, par la suite, vous réappliquez le thème, toute mise en forme manuelle est mise en forme et la forme prend l’ensemble de la mise en forme du thème.</span><span class="sxs-lookup"><span data-stu-id="881f2-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="881f2-115">**ISTHEMED** prend la valeur TRUE si la cellule [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forme est supérieure à 0.</span><span class="sxs-lookup"><span data-stu-id="881f2-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="881f2-116">Si cette cellule est égale à 0, **ISTHEMED** est évalué à FALSE.</span><span class="sxs-lookup"><span data-stu-id="881f2-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="881f2-117">Le thème de la feuille de document et de la feuille page n’affecte pas la valeur de la **fonction ISTHEMED** utilisée dans une feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="881f2-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="881f2-118">Le thème de la page n’a d’importance que si la fonction **ISTHEMED** s’affiche dans la feuille de page.</span><span class="sxs-lookup"><span data-stu-id="881f2-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="881f2-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="881f2-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="881f2-120">Cell</span><span class="sxs-lookup"><span data-stu-id="881f2-120">Cell</span></span>  <br/> |<span data-ttu-id="881f2-121">Formule</span><span class="sxs-lookup"><span data-stu-id="881f2-121">Formula</span></span>  <br/> |<span data-ttu-id="881f2-122">Résultat</span><span class="sxs-lookup"><span data-stu-id="881f2-122">Result</span></span>  <br/> |
|<span data-ttu-id="881f2-123">Char.Font</span><span class="sxs-lookup"><span data-stu-id="881f2-123">Char.Font</span></span>  <br/> |<span data-ttu-id="881f2-124">IF(ISTHEMED(), THEMEVAL(), FONT(« Calibri »))</span><span class="sxs-lookup"><span data-stu-id="881f2-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="881f2-125">Si un thème est appliqué à la forme, le texte de la forme accepte la mise en forme de police du thème.</span><span class="sxs-lookup"><span data-stu-id="881f2-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="881f2-126">Si la forme n’est pas un modèle, le texte de la forme est formaté avec la police « Calibri ».</span><span class="sxs-lookup"><span data-stu-id="881f2-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="881f2-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="881f2-127">LineColor</span></span>  <br/> |<span data-ttu-id="881f2-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="881f2-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="881f2-129">Si un themed est appliqué à la forme, la couleur de trait de la forme est rouge.</span><span class="sxs-lookup"><span data-stu-id="881f2-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="881f2-130">Si la forme n’est pas sur le themed, la couleur de trait de la forme est verte.</span><span class="sxs-lookup"><span data-stu-id="881f2-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

