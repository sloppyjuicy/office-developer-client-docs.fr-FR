---
title: Fonction ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Renvoie une valeur de type Boolean qui indique si un thème est appliqué à une forme.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357511"
---
# <a name="isthemed-function"></a><span data-ttu-id="8a2f7-103">Fonction ISTHEMED</span><span class="sxs-lookup"><span data-stu-id="8a2f7-103">ISTHEMED Function</span></span>

<span data-ttu-id="8a2f7-104">Renvoie une valeur de type Boolean qui indique si un thème est appliqué à une forme.</span><span class="sxs-lookup"><span data-stu-id="8a2f7-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="8a2f7-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="8a2f7-105">Version Information</span></span>

<span data-ttu-id="8a2f7-106">Version ajoutée : Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="8a2f7-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8a2f7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a2f7-107">Syntax</span></span>

 <span data-ttu-id="8a2f7-108">**ISTHEMED** ()</span><span class="sxs-lookup"><span data-stu-id="8a2f7-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="8a2f7-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8a2f7-109">Return value</span></span>

<span data-ttu-id="8a2f7-110">Booléen</span><span class="sxs-lookup"><span data-stu-id="8a2f7-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a2f7-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a2f7-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="8a2f7-112">La fonction **ISTHEMED** dans Visio 2013 remplace la fonction **CELLISTHEMED** des versions précédentes de Visio.</span><span class="sxs-lookup"><span data-stu-id="8a2f7-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="8a2f7-113">La fonction **ISTHEMED** vous permet d'affecter des parties appropriées de la mise en forme d'un thème à une forme, tout en conservant la possibilité de remplacer les autres parties de la mise en forme de thème par une mise en forme manuelle.</span><span class="sxs-lookup"><span data-stu-id="8a2f7-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="8a2f7-114">Si, par la suite, vous réappliquez le thème, toute mise en forme manuelle est remplacée et la forme prend la mise en forme du thème.</span><span class="sxs-lookup"><span data-stu-id="8a2f7-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="8a2f7-115">**ISTHEMED** renvoie la valeur true si la cellule [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forme est supérieure à 0.</span><span class="sxs-lookup"><span data-stu-id="8a2f7-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="8a2f7-116">Si cette cellule est égale à 0, **ISTHEMED** prend la valeur false.</span><span class="sxs-lookup"><span data-stu-id="8a2f7-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="8a2f7-117">Le thème de DocumentSheet et PageSheet n'affecte pas la valeur de la fonction **ISTHEMED** utilisée dans une feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8a2f7-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="8a2f7-118">Uniquement si la fonction **ISTHEMED** s'affiche dans la PageSheet fait le thème de la page.</span><span class="sxs-lookup"><span data-stu-id="8a2f7-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8a2f7-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="8a2f7-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="8a2f7-120">Cell</span><span class="sxs-lookup"><span data-stu-id="8a2f7-120">Cell</span></span>  <br/> |<span data-ttu-id="8a2f7-121">Formule</span><span class="sxs-lookup"><span data-stu-id="8a2f7-121">Formula</span></span>  <br/> |<span data-ttu-id="8a2f7-122">Résultat</span><span class="sxs-lookup"><span data-stu-id="8a2f7-122">Result</span></span>  <br/> |
|<span data-ttu-id="8a2f7-123">Char. font</span><span class="sxs-lookup"><span data-stu-id="8a2f7-123">Char.Font</span></span>  <br/> |<span data-ttu-id="8a2f7-124">IF (ISTHEMED (), THEMEVAL (), FONT ("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="8a2f7-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="8a2f7-125">Si des thèmes sont appliqués à la forme, le texte de la forme accepte la mise en forme de la police du thème.</span><span class="sxs-lookup"><span data-stu-id="8a2f7-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="8a2f7-126">Si la forme n'est pas à thème, le texte de la forme est mis en forme avec la police «Calibri».</span><span class="sxs-lookup"><span data-stu-id="8a2f7-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="8a2f7-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="8a2f7-127">LineColor</span></span>  <br/> |<span data-ttu-id="8a2f7-128">SI (ISTHEMED, RGB (255, 0, 0), RVB (0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="8a2f7-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="8a2f7-129">Si des thèmes sont appliqués à la forme, la couleur de trait de la forme est rouge.</span><span class="sxs-lookup"><span data-stu-id="8a2f7-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="8a2f7-130">Si la forme n'est pas à thème, la couleur de trait de la forme est verte.</span><span class="sxs-lookup"><span data-stu-id="8a2f7-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

