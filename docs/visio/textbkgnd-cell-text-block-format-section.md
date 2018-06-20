---
title: TextBkgnd, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Détermine la couleur d'arrière-plan du texte dans une forme.
ms.openlocfilehash: 2256a4c89812924af820c020c225f4b82b1d4856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789887"
---
# <a name="textbkgnd-cell-text-block-format-section"></a><span data-ttu-id="bab60-103">TextBkgnd, cellule (section Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="bab60-103">TextBkgnd Cell (Text Block Format Section)</span></span>

<span data-ttu-id="bab60-104">Détermine la couleur d'arrière-plan du texte dans une forme.</span><span class="sxs-lookup"><span data-stu-id="bab60-104">Determines the text background color for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bab60-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="bab60-105">Remarks</span></span>

<span data-ttu-id="bab60-106">La cellule TextBkgnd peut avoir n’importe quelle valeur comprise entre 0 et 24, ou 255.</span><span class="sxs-lookup"><span data-stu-id="bab60-106">The TextBkgnd cell can have any value from 0 through 24, or 255.</span></span> <span data-ttu-id="bab60-107">Les valeurs 0 et 255 ( *visTxtBlklOpaque correspondent toutes*) indiquent un arrière-plan de texte transparent.</span><span class="sxs-lookup"><span data-stu-id="bab60-107">The values 0 and 255 ( *visTxtBlklOpaque*) both indicate a transparent text background.</span></span> 
  
<span data-ttu-id="bab60-108">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL plus un — par exemple, RVB (255,127,255) + 1.</span><span class="sxs-lookup"><span data-stu-id="bab60-108">To enter a custom color, use the RGB or HSL function plus one—for example, RGB(255,127,255)+1.</span></span> <span data-ttu-id="bab60-109">La valeur d’une couleur personnalisée est sa couleur RVB et RVB ( *r, g, b*) + 1, au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="bab60-109">The value of a custom color is its RGB color, and RGB( *r, g, b*)+1, rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="bab60-110">Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 25 et supérieures.</span><span class="sxs-lookup"><span data-stu-id="bab60-110">When used in numeric operations, custom colors have values of 25 and above.</span></span> 
  
<span data-ttu-id="bab60-111">Vous pouvez définir la transparence de la couleur du texte d'arrière-plan dans la cellule TextBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="bab60-111">You can set the transparency of the text background color in the TextBkgndTrans cell.</span></span>
  
<span data-ttu-id="bab60-112">Pour obtenir une référence à la cellule TextBkgnd par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="bab60-112">To get a reference to the TextBkgnd cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bab60-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bab60-113">Cell name:</span></span>  <br/> |<span data-ttu-id="bab60-114">TextBkgnd</span><span class="sxs-lookup"><span data-stu-id="bab60-114">TextBkgnd</span></span>  <br/> |
   
<span data-ttu-id="bab60-115">Pour obtenir une référence à la cellule TextBkgnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bab60-115">To get a reference to the TextBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bab60-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bab60-116">Section index:</span></span>  <br/> |<span data-ttu-id="bab60-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bab60-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bab60-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bab60-118">Row index:</span></span>  <br/> |<span data-ttu-id="bab60-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="bab60-119">**visRowText**</span></span> <br/> |
|<span data-ttu-id="bab60-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bab60-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bab60-121">**visTxtBlkBkgnd**</span><span class="sxs-lookup"><span data-stu-id="bab60-121">**visTxtBlkBkgnd**</span></span> <br/> |
   

