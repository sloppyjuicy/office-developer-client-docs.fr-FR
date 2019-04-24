---
title: ShdwForegnd, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Détermine la couleur du premier plan (traits) du motif de remplissage de l'ombre portée de la forme.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349104"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="fdeaf-103">ShdwForegnd, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="fdeaf-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="fdeaf-104">Détermine la couleur du premier plan (traits) du motif de remplissage de l'ombre portée de la forme.</span><span class="sxs-lookup"><span data-stu-id="fdeaf-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fdeaf-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="fdeaf-105">Remarks</span></span>

<span data-ttu-id="fdeaf-106">Pour définir la couleur, entrez une valeur comprise entre 0 et 23, correspondant à un index d’un ensemble de couleurs.</span><span class="sxs-lookup"><span data-stu-id="fdeaf-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="fdeaf-107">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL.</span><span class="sxs-lookup"><span data-stu-id="fdeaf-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="fdeaf-108">La valeur d'une couleur personnalisée est sa couleur RVB et la valeur RVB ( *r, v, b*), au lieu d'un nombre, est affichée dans la fenêtre feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fdeaf-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="fdeaf-109">Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24.</span><span class="sxs-lookup"><span data-stu-id="fdeaf-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="fdeaf-110">Vous pouvez définir la transparence de la couleur de premier plan du motif de remplissage de l'ombre portée d'une forme dans la cellule ShdwForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="fdeaf-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="fdeaf-111">Pour obtenir une référence à la cellule ShdwForegnd par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="fdeaf-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdeaf-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fdeaf-112">Cell name:</span></span>  <br/> | <span data-ttu-id="fdeaf-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="fdeaf-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="fdeaf-114">Pour obtenir une référence à la cellule ShdwForegnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="fdeaf-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fdeaf-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fdeaf-115">Section index:</span></span>  <br/> |<span data-ttu-id="fdeaf-116">**Définis**</span><span class="sxs-lookup"><span data-stu-id="fdeaf-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fdeaf-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fdeaf-117">Row index:</span></span>  <br/> |<span data-ttu-id="fdeaf-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="fdeaf-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="fdeaf-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fdeaf-119">Cell index:</span></span>  <br/> |<span data-ttu-id="fdeaf-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="fdeaf-120">**visFillShdwForegnd**</span></span> <br/> |
   

