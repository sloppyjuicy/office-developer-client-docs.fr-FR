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
ms.openlocfilehash: 352fecf8d99069cfb5ebd72d295284dc03446364
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415564"
---
# <a name="fillforegnd-cell-fill-format-section"></a><span data-ttu-id="1d91c-103">FillForegnd, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="1d91c-103">FillForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="1d91c-104">Détermine la couleur du premier plan (traits) du motif de remplissage de la forme.</span><span class="sxs-lookup"><span data-stu-id="1d91c-104">Determines the color used for the foreground (stroke) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d91c-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d91c-105">Remarks</span></span>

<span data-ttu-id="1d91c-106">Pour définir la couleur, tapez un nombre compris entre 0 et 23.</span><span class="sxs-lookup"><span data-stu-id="1d91c-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="1d91c-107">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL.</span><span class="sxs-lookup"><span data-stu-id="1d91c-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="1d91c-108">La valeur d'une couleur personnalisée est sa couleur RVB et la valeur RVB ( *r, v, b*), au lieu d'un nombre, est affichée dans la fenêtre feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1d91c-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="1d91c-109">Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24.</span><span class="sxs-lookup"><span data-stu-id="1d91c-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="1d91c-110">Vous pouvez définir la transparence de remplissage de premier plan dans la cellule TransPremPlanRempl.</span><span class="sxs-lookup"><span data-stu-id="1d91c-110">You can set the transparency of the foreground fill in the FillForegndTrans cell.</span></span>
  
<span data-ttu-id="1d91c-111">Pour obtenir une référence à la cellule FillForegnd par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="1d91c-111">To get a reference to the FillForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d91c-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1d91c-112">Cell name:</span></span>  <br/> |<span data-ttu-id="1d91c-113">FillForegnd</span><span class="sxs-lookup"><span data-stu-id="1d91c-113">FillForegnd</span></span>  <br/> |
   
<span data-ttu-id="1d91c-114">Pour obtenir une référence à la cellule FillForegnd à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1d91c-114">To get a reference to the FillForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d91c-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1d91c-115">Section index:</span></span>  <br/> |<span data-ttu-id="1d91c-116">**Définis**</span><span class="sxs-lookup"><span data-stu-id="1d91c-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1d91c-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1d91c-117">Row index:</span></span>  <br/> |<span data-ttu-id="1d91c-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="1d91c-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="1d91c-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1d91c-119">Cell index:</span></span>  <br/> |<span data-ttu-id="1d91c-120">**visFillForegnd**</span><span class="sxs-lookup"><span data-stu-id="1d91c-120">**visFillForegnd**</span></span> <br/> |
   

