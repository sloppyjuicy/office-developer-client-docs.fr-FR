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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422249"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="ef21a-103">ShdwForegnd, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="ef21a-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="ef21a-104">Détermine la couleur du premier plan (traits) du motif de remplissage de l'ombre portée de la forme.</span><span class="sxs-lookup"><span data-stu-id="ef21a-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef21a-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="ef21a-105">Remarks</span></span>

<span data-ttu-id="ef21a-106">Pour définir la couleur, entrez une valeur comprise entre 0 et 23, correspondant à un index d’un ensemble de couleurs.</span><span class="sxs-lookup"><span data-stu-id="ef21a-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="ef21a-107">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL.</span><span class="sxs-lookup"><span data-stu-id="ef21a-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="ef21a-108">La valeur d’une couleur personnalisée est sa couleur RVB, et RVB( *r, g, b*), plutôt qu’un nombre, s’affiche dans la fenêtre Feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ef21a-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="ef21a-109">Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24.</span><span class="sxs-lookup"><span data-stu-id="ef21a-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="ef21a-110">Vous pouvez définir la transparence de la couleur de premier plan du motif de remplissage de l'ombre portée d'une forme dans la cellule ShdwForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="ef21a-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="ef21a-111">Pour obtenir une référence à la cellule ShdwForegnd par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ef21a-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ef21a-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ef21a-112">Cell name:</span></span>  <br/> | <span data-ttu-id="ef21a-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="ef21a-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="ef21a-114">Pour obtenir une référence à la cellule ShdwForegnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ef21a-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ef21a-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ef21a-115">Section index:</span></span>  <br/> |<span data-ttu-id="ef21a-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ef21a-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ef21a-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ef21a-117">Row index:</span></span>  <br/> |<span data-ttu-id="ef21a-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="ef21a-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="ef21a-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ef21a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="ef21a-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="ef21a-120">**visFillShdwForegnd**</span></span> <br/> |
   

