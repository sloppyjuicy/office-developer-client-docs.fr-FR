---
title: PageScale, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: Détermine la valeur de l'unité de page dans l'échelle de dessin en cours. L'échelle de dessin est le rapport entre l'unité de page représentée dans la cellule PageScale et l'unité de dessin représentée dans la cellule DrawingScale.
ms.openlocfilehash: 0e1721ea667ad3bcd9f35880ab4e63bc90802c32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789247"
---
# <a name="pagescale-cell-page-properties-section"></a><span data-ttu-id="994e7-104">PageScale, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="994e7-104">PageScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="994e7-p102">Détermine la valeur de l'unité de page dans l'échelle de dessin en cours. L'échelle de dessin est le rapport entre l'unité de page représentée dans la cellule PageScale et l'unité de dessin représentée dans la cellule DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="994e7-p102">Determines the value of the page unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="994e7-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="994e7-107">Remarks</span></span>

<span data-ttu-id="994e7-108">Vous pouvez également définir la valeur de la cellule PageScale sous l’onglet **À l’échelle de dessin** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ).</span><span class="sxs-lookup"><span data-stu-id="994e7-108">You can also set the value of the PageScale cell on the **Drawing Scale** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="994e7-109">La valeur de la cellule est le premier des deux nombres dans la zone **échelle prédéfinie** ou **échelle personnalisée** , selon le paramètre à l’échelle de dessin sélectionné sous **échelle du dessin**.</span><span class="sxs-lookup"><span data-stu-id="994e7-109">The value of the cell is the first of the two numbers in the **Pre-defined scale** box or **Custom scale** box, depending on the drawing scale setting selected under **Drawing scale**.</span></span> <span data-ttu-id="994e7-110">Par exemple, si vous sélectionnez une échelle architecturale pour votre dessin, l’échelle de la page de dessin est 3/32 "= 1'0".</span><span class="sxs-lookup"><span data-stu-id="994e7-110">For example, if you select an architectural scale for your drawing, the drawing scale for the page is 3/32" = 1'0".</span></span> <span data-ttu-id="994e7-111">La valeur de la cellule PageScale est en 0.0938.</span><span class="sxs-lookup"><span data-stu-id="994e7-111">The value in the PageScale cell is 0.0938 in.</span></span> <span data-ttu-id="994e7-112">(ou 3/32") et la valeur de la cellule DrawingScale est ft 1.</span><span class="sxs-lookup"><span data-stu-id="994e7-112">(or 3/32") and the value in the DrawingScale cell is 1 ft.</span></span>
  
<span data-ttu-id="994e7-113">Pour obtenir une référence à la cellule PageScale par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="994e7-113">To get a reference to the PageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="994e7-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="994e7-114">Cell name:</span></span>  <br/> |<span data-ttu-id="994e7-115">PageScale</span><span class="sxs-lookup"><span data-stu-id="994e7-115">PageScale</span></span>  <br/> |
   
<span data-ttu-id="994e7-116">Pour obtenir une référence à la cellule PageScale par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="994e7-116">To get a reference to the PageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="994e7-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="994e7-117">Section index:</span></span>  <br/> |<span data-ttu-id="994e7-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="994e7-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="994e7-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="994e7-119">Row index:</span></span>  <br/> |<span data-ttu-id="994e7-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="994e7-120">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="994e7-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="994e7-121">Cell index:</span></span>  <br/> |<span data-ttu-id="994e7-122">**visPageScale**</span><span class="sxs-lookup"><span data-stu-id="994e7-122">**visPageScale**</span></span> <br/> |
   

