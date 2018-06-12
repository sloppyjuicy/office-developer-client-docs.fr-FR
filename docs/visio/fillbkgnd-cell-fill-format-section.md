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
ms.openlocfilehash: d1222026887313d7737a3a0ded9e798e9bf5ea30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788617"
---
# <a name="fillbkgnd-cell-fill-format-section"></a><span data-ttu-id="df0dc-103">FillBkgnd, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="df0dc-103">FillBkgnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="df0dc-104">Détermine la couleur d'arrière-plan (remplissage) du motif de remplissage de la forme.</span><span class="sxs-lookup"><span data-stu-id="df0dc-104">Determines the color used for the background (fill) of the shape's fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df0dc-105">Note</span><span class="sxs-lookup"><span data-stu-id="df0dc-105">Remarks</span></span>

<span data-ttu-id="df0dc-106">Pour définir la couleur, tapez un nombre compris entre 0 et 23.</span><span class="sxs-lookup"><span data-stu-id="df0dc-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="df0dc-107">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL.</span><span class="sxs-lookup"><span data-stu-id="df0dc-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="df0dc-108">La valeur d’une couleur personnalisée est sa couleur RVB et RVB (*r, g, b*), au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="df0dc-108">The value of a custom color is its RGB color, and RGB(*r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="df0dc-109">Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 24 et au-dessus.</span><span class="sxs-lookup"><span data-stu-id="df0dc-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="df0dc-110">Vous pouvez définir la transparence de remplissage de l'arrière-plan dans la cellule FillBkgndTrans.</span><span class="sxs-lookup"><span data-stu-id="df0dc-110">You can set the transparency of the background fill in the FillBkgndTrans cell.</span></span> 
  
<span data-ttu-id="df0dc-111">Pour obtenir une référence à la cellule FillBkgnd par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="df0dc-111">To get a reference to the FillBkgnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df0dc-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="df0dc-112">Cell name:</span></span>  <br/> | <span data-ttu-id="df0dc-113">FillBkgnd</span><span class="sxs-lookup"><span data-stu-id="df0dc-113">FillBkgnd</span></span>  <br/> |
   
<span data-ttu-id="df0dc-114">Pour obtenir une référence à la cellule FillBkgnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="df0dc-114">To get a reference to the FillBkgnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df0dc-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="df0dc-115">Section index:</span></span>  <br/> |<span data-ttu-id="df0dc-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="df0dc-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="df0dc-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="df0dc-117">Row index:</span></span>  <br/> |<span data-ttu-id="df0dc-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="df0dc-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="df0dc-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="df0dc-119">Cell index:</span></span>  <br/> |<span data-ttu-id="df0dc-120">**visFillBkgnd**</span><span class="sxs-lookup"><span data-stu-id="df0dc-120">**visFillBkgnd**</span></span> <br/> |
   

