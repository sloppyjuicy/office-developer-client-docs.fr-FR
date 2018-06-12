---
title: FillForegnd, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Détermine la couleur du premier plan (traits) du motif de remplissage de la forme.
ms.openlocfilehash: 27126457963e4e55419b0cac5baf1eab08fe3cc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788638"
---
# <a name="fillforegnd-cell-fill-format-section"></a><span data-ttu-id="44826-103">FillForegnd, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="44826-103">FillForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="44826-104">Détermine la couleur du premier plan (traits) du motif de remplissage de la forme.</span><span class="sxs-lookup"><span data-stu-id="44826-104">Determines the color used for the foreground (stroke) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44826-105">Note</span><span class="sxs-lookup"><span data-stu-id="44826-105">Remarks</span></span>

<span data-ttu-id="44826-106">Pour définir la couleur, tapez un nombre compris entre 0 et 23.</span><span class="sxs-lookup"><span data-stu-id="44826-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="44826-107">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL.</span><span class="sxs-lookup"><span data-stu-id="44826-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="44826-108">La valeur d’une couleur personnalisée est sa couleur RVB et RVB ( *r, g, b*), au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="44826-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="44826-109">Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 24 et au-dessus.</span><span class="sxs-lookup"><span data-stu-id="44826-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="44826-110">Vous pouvez définir la transparence de remplissage de premier plan dans la cellule TransPremPlanRempl.</span><span class="sxs-lookup"><span data-stu-id="44826-110">You can set the transparency of the foreground fill in the FillForegndTrans cell.</span></span>
  
<span data-ttu-id="44826-111">Pour obtenir une référence à la cellule FillForegnd par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="44826-111">To get a reference to the FillForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44826-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="44826-112">Cell name:</span></span>  <br/> |<span data-ttu-id="44826-113">FillForegnd</span><span class="sxs-lookup"><span data-stu-id="44826-113">FillForegnd</span></span>  <br/> |
   
<span data-ttu-id="44826-114">Pour obtenir une référence à la cellule FillForegnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="44826-114">To get a reference to the FillForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44826-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="44826-115">Section index:</span></span>  <br/> |<span data-ttu-id="44826-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="44826-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="44826-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="44826-117">Row index:</span></span>  <br/> |<span data-ttu-id="44826-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="44826-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="44826-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="44826-119">Cell index:</span></span>  <br/> |<span data-ttu-id="44826-120">**visFillForegnd**</span><span class="sxs-lookup"><span data-stu-id="44826-120">**visFillForegnd**</span></span> <br/> |
   

