---
title: FillBkgnd, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Détermine la couleur d'arrière-plan (remplissage) du motif de remplissage de la forme.
ms.openlocfilehash: f4df5d2b44a50380c996b9b2e0f7cda7d212093b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436642"
---
# <a name="fillbkgnd-cell-fill-format-section"></a><span data-ttu-id="f7885-103">FillBkgnd, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="f7885-103">FillBkgnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="f7885-104">Détermine la couleur d'arrière-plan (remplissage) du motif de remplissage de la forme.</span><span class="sxs-lookup"><span data-stu-id="f7885-104">Determines the color used for the background (fill) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7885-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7885-105">Remarks</span></span>

<span data-ttu-id="f7885-106">Pour définir la couleur, tapez un nombre compris entre 0 et 23.</span><span class="sxs-lookup"><span data-stu-id="f7885-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="f7885-p101">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d'une couleur personnalisée est sa valeur RVB et la fenêtre Feuille ShapeSheet affiche RVB (*r, v, b*) au lieu d'une valeur. Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24.</span><span class="sxs-lookup"><span data-stu-id="f7885-p101">To enter a custom color, use the RGB or HSL function. The value of a custom color is its RGB color, and RGB(*r, g, b*), rather than a number, will be shown in the ShapeSheet window. When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="f7885-110">Vous pouvez définir la transparence de remplissage de l'arrière-plan dans la cellule FillBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="f7885-110">You can set the transparency of the background fill in the FillBkgndTrans cell.</span></span> 
  
<span data-ttu-id="f7885-111">Pour obtenir une référence à la cellule FillBkgnd par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f7885-111">To get a reference to the FillBkgnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7885-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f7885-112">Cell name:</span></span>  <br/> | <span data-ttu-id="f7885-113">FillBkgnd</span><span class="sxs-lookup"><span data-stu-id="f7885-113">FillBkgnd</span></span>  <br/> |
   
<span data-ttu-id="f7885-114">Pour obtenir une référence à la cellule FillBkgnd à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f7885-114">To get a reference to the FillBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f7885-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f7885-115">Section index:</span></span>  <br/> |<span data-ttu-id="f7885-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f7885-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f7885-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f7885-117">Row index:</span></span>  <br/> |<span data-ttu-id="f7885-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="f7885-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="f7885-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f7885-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f7885-120">**visFillBkgnd**</span><span class="sxs-lookup"><span data-stu-id="f7885-120">**visFillBkgnd**</span></span> <br/> |
   

