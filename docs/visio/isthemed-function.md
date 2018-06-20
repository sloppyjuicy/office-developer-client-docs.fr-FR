---
title: Fonction ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Renvoie une valeur Boolean indiquant si une forme possède un thème est appliqué.
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788892"
---
# <a name="isthemed-function"></a><span data-ttu-id="91c29-103">Fonction ISTHEMED</span><span class="sxs-lookup"><span data-stu-id="91c29-103">ISTHEMED Function</span></span>

<span data-ttu-id="91c29-104">Renvoie une valeur Boolean indiquant si une forme possède un thème est appliqué.</span><span class="sxs-lookup"><span data-stu-id="91c29-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="91c29-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="91c29-105">Version Information</span></span>

<span data-ttu-id="91c29-106">Version ajoutée : Visio 2013</span><span class="sxs-lookup"><span data-stu-id="91c29-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="91c29-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91c29-107">Syntax</span></span>

 <span data-ttu-id="91c29-108">**ISTHEMED** ()</span><span class="sxs-lookup"><span data-stu-id="91c29-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="91c29-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="91c29-109">Return value</span></span>

<span data-ttu-id="91c29-110">Booléenne</span><span class="sxs-lookup"><span data-stu-id="91c29-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91c29-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="91c29-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="91c29-112">La fonction **ISTHEMED** dans Visio 2013 remplace la fonction **CELLISTHEMED** à partir de versions antérieures de Visio.</span><span class="sxs-lookup"><span data-stu-id="91c29-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="91c29-113">**ISTHEMED** permet d’affecter les aspects de la mise en forme d’un thème à une forme de fonction tout en conservant la possibilité de remplacer les autres composants du thème de la mise en forme appliquée manuellement la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="91c29-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="91c29-114">Si vous réappliquez ensuite le thème, toute mise en forme manuelle est remplacé et toute la mise en forme du thème prend la forme.</span><span class="sxs-lookup"><span data-stu-id="91c29-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="91c29-115">**ISTHEMED** renvoie la valeur TRUE si la cellule [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) de la forme est supérieure à 0.</span><span class="sxs-lookup"><span data-stu-id="91c29-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="91c29-116">Si cette cellule est égale à 0, **ISTHEMED** a la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="91c29-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="91c29-117">Le thème de la propriété DocumentSheet et PageSheet n’affecte pas la valeur de la fonction **ISTHEMED** utilisée dans une feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="91c29-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="91c29-118">Uniquement si la fonction **ISTHEMED** s’affiche dans le PageSheet n’en matière de thème de la page.</span><span class="sxs-lookup"><span data-stu-id="91c29-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="91c29-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="91c29-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="91c29-120">Cellule</span><span class="sxs-lookup"><span data-stu-id="91c29-120">Cell</span></span>  <br/> |<span data-ttu-id="91c29-121">Formule</span><span class="sxs-lookup"><span data-stu-id="91c29-121">Formula</span></span>  <br/> |<span data-ttu-id="91c29-122">Résultat</span><span class="sxs-lookup"><span data-stu-id="91c29-122">Result</span></span>  <br/> |
|<span data-ttu-id="91c29-123">Char.Font</span><span class="sxs-lookup"><span data-stu-id="91c29-123">Char.Font</span></span>  <br/> |<span data-ttu-id="91c29-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="91c29-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="91c29-125">Si la forme possède un thème appliqué, le texte de la forme accepte la mise en forme du thème de police.</span><span class="sxs-lookup"><span data-stu-id="91c29-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="91c29-126">Si la forme n’est pas à thème, le texte de la forme est mise en forme avec la police « Calibri ».</span><span class="sxs-lookup"><span data-stu-id="91c29-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="91c29-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="91c29-127">LineColor</span></span>  <br/> |<span data-ttu-id="91c29-128">IF (ISTHEMED, RVB (255, 0, 0), RVB (0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="91c29-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="91c29-129">Si la forme possède un thème appliqué, la couleur de trait de la forme est rouge.</span><span class="sxs-lookup"><span data-stu-id="91c29-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="91c29-130">Si la forme n’est pas à thème, la couleur de trait de la forme est verte.</span><span class="sxs-lookup"><span data-stu-id="91c29-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

