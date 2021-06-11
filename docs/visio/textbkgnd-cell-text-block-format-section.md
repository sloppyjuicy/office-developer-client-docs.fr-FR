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
ms.openlocfilehash: 2450bf0cb0e013c0f9310eacfca0f5a20e7e6063
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406541"
---
# <a name="textbkgnd-cell-text-block-format-section"></a><span data-ttu-id="18849-103">TextBkgnd, cellule (section Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="18849-103">TextBkgnd Cell (Text Block Format Section)</span></span>

<span data-ttu-id="18849-104">Détermine la couleur d'arrière-plan du texte dans une forme.</span><span class="sxs-lookup"><span data-stu-id="18849-104">Determines the text background color for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18849-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="18849-105">Remarks</span></span>

<span data-ttu-id="18849-106">La cellule TextBkgnd peut avoir une valeur comprise entre 0 et 24, ou 255.</span><span class="sxs-lookup"><span data-stu-id="18849-106">The TextBkgnd cell can have any value from 0 through 24, or 255.</span></span> <span data-ttu-id="18849-107">Les valeurs 0 et 255 *(visTxtBlklOpaque)* indiquent toutes deux un arrière-plan de texte transparent.</span><span class="sxs-lookup"><span data-stu-id="18849-107">The values 0 and 255 ( *visTxtBlklOpaque*) both indicate a transparent text background.</span></span> 
  
<span data-ttu-id="18849-108">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL plus un : par exemple RVB(255,127,255) +1.</span><span class="sxs-lookup"><span data-stu-id="18849-108">To enter a custom color, use the RGB or HSL function plus one—for example, RGB(255,127,255)+1.</span></span> <span data-ttu-id="18849-109">La valeur d’une couleur personnalisée est sa couleur RVB, et RVB( *r, g, b*)+1, au lieu d’un nombre, s’affiche dans la fenêtre Feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="18849-109">The value of a custom color is its RGB color, and RGB( *r, g, b*)+1, rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="18849-110">Lorsqu'elles sont utilisées dans les opérations numériques, les couleurs personnalisées ont des valeurs de 25 et supérieures.</span><span class="sxs-lookup"><span data-stu-id="18849-110">When used in numeric operations, custom colors have values of 25 and above.</span></span> 
  
<span data-ttu-id="18849-111">Vous pouvez définir la transparence de la couleur du texte d'arrière-plan dans la cellule TextBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="18849-111">You can set the transparency of the text background color in the TextBkgndTrans cell.</span></span>
  
<span data-ttu-id="18849-112">Pour obtenir une référence à la cellule TextBkgnd par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="18849-112">To get a reference to the TextBkgnd cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18849-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="18849-113">Cell name:</span></span>  <br/> |<span data-ttu-id="18849-114">TextBkgnd</span><span class="sxs-lookup"><span data-stu-id="18849-114">TextBkgnd</span></span>  <br/> |
   
<span data-ttu-id="18849-115">Pour obtenir une référence à la cellule TextBkgnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="18849-115">To get a reference to the TextBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18849-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="18849-116">Section index:</span></span>  <br/> |<span data-ttu-id="18849-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="18849-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="18849-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="18849-118">Row index:</span></span>  <br/> |<span data-ttu-id="18849-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="18849-119">**visRowText**</span></span> <br/> |
|<span data-ttu-id="18849-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="18849-120">Cell index:</span></span>  <br/> |<span data-ttu-id="18849-121">**visTxtBlkBkgnd**</span><span class="sxs-lookup"><span data-stu-id="18849-121">**visTxtBlkBkgnd**</span></span> <br/> |
   

