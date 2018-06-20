---
title: ShapeShdwScaleFactor, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Indique le pourcentage d'agrandissement ou de réduction possible de l'ombre d'une forme.
ms.openlocfilehash: 0b6392030e7efc8ea36c8d728b99c9b82482840b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789684"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="00653-103">ShapeShdwScaleFactor, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="00653-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="00653-104">Indique le pourcentage d'agrandissement ou de réduction possible de l'ombre d'une forme.</span><span class="sxs-lookup"><span data-stu-id="00653-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00653-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="00653-105">Remarks</span></span>

<span data-ttu-id="00653-106">Chaque ombre a un axe d’ombre, qui est un point sur l’ombre qui correspond à l’axe de la forme.</span><span class="sxs-lookup"><span data-stu-id="00653-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="00653-107">Par exemple, si le code confidentiel d’une forme est au centre de la forme, alors l’emplacement de l’axe est le point central de l’ombre.</span><span class="sxs-lookup"><span data-stu-id="00653-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="00653-108">Lors de l’application à l’échelle à des ombres simples, l’agrandissement est centré à l’emplacement de l’axe ; lors de l’application à l’échelle à des ombres obliques, facteur d’agrandissement est appliqué dans la direction oblique.</span><span class="sxs-lookup"><span data-stu-id="00653-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="00653-109">Pour définir cette valeur pour toutes les formes d'une page, utilisez la cellule ShdwScaleFactor de la section Page Properties.</span><span class="sxs-lookup"><span data-stu-id="00653-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="00653-110">Cette valeur correspond à la valeur du paramètre **facteur d’agrandissement** de la boîte de dialogue **ombre** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **ombre**, puis cliquez sur **Options d’ombres**).</span><span class="sxs-lookup"><span data-stu-id="00653-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="00653-111">Pour obtenir une référence à la cellule ShapeShdwScaleFactor par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="00653-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00653-112">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="00653-112">Cell name:</span></span>  <br/> |<span data-ttu-id="00653-113">ShapeShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="00653-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="00653-114">Pour obtenir une référence à la cellule ShapeShdwScaleFactor par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="00653-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00653-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="00653-115">Section index:</span></span>  <br/> |<span data-ttu-id="00653-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="00653-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="00653-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="00653-117">Row index:</span></span>  <br/> |<span data-ttu-id="00653-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="00653-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="00653-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="00653-119">Cell index:</span></span>  <br/> |<span data-ttu-id="00653-120">**visFillShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="00653-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

