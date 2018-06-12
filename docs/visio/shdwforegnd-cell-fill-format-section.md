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
ms.openlocfilehash: f39109a296949d23142017661bb55f0708402d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789708"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="8cc8d-103">ShdwForegnd, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="8cc8d-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="8cc8d-104">Détermine la couleur du premier plan (traits) du motif de remplissage de l'ombre portée de la forme.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8cc8d-105">Note</span><span class="sxs-lookup"><span data-stu-id="8cc8d-105">Remarks</span></span>

<span data-ttu-id="8cc8d-106">Pour définir la couleur, entrez une valeur comprise entre 0 et 23, correspondant à un index d’un ensemble de couleurs.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="8cc8d-107">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="8cc8d-108">La valeur d’une couleur personnalisée est sa couleur RVB et RVB ( *r, g, b*), au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="8cc8d-109">Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 24 et au-dessus.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="8cc8d-110">Vous pouvez définir la transparence de la couleur de premier plan du motif de remplissage de l'ombre portée d'une forme dans la cellule ShdwForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="8cc8d-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="8cc8d-111">Pour obtenir une référence à la cellule ShdwForegnd par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="8cc8d-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8cc8d-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8cc8d-112">Cell name:</span></span>  <br/> | <span data-ttu-id="8cc8d-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="8cc8d-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="8cc8d-114">Pour obtenir une référence à la cellule ShdwForegnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8cc8d-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8cc8d-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8cc8d-115">Section index:</span></span>  <br/> |<span data-ttu-id="8cc8d-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8cc8d-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8cc8d-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8cc8d-117">Row index:</span></span>  <br/> |<span data-ttu-id="8cc8d-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="8cc8d-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="8cc8d-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8cc8d-119">Cell index:</span></span>  <br/> |<span data-ttu-id="8cc8d-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="8cc8d-120">**visFillShdwForegnd**</span></span> <br/> |
   

