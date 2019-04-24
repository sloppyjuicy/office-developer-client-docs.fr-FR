---
title: Y, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026934
localization_priority: Normal
ms.assetid: b213fc46-7f80-99fd-60ba-8ddf3d0f6ee3
description: Position de la coordonnée y dans les coordonnées locales de la forme et entourant laquelle se trouve le bouton de balise d'action.
ms.openlocfilehash: 02797a849a262cb506f4617aadaccedabccdab77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341321"
---
# <a name="y-cell-action-tags-section"></a><span data-ttu-id="97ba2-103">Y, cellule (section Action Tags)</span><span class="sxs-lookup"><span data-stu-id="97ba2-103">Y Cell (Action Tags Section)</span></span>

<span data-ttu-id="97ba2-104">Position de la coordonnée *y* dans les coordonnées locales de la forme et entourant laquelle se trouve le bouton de balise d'action.</span><span class="sxs-lookup"><span data-stu-id="97ba2-104">The  *y*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="97ba2-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="97ba2-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="97ba2-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="97ba2-106">Remarks</span></span>

<span data-ttu-id="97ba2-107">Les cellules X et Y définissent un point dans le système de coordonnées locales de la forme, tandis que les cellules X Justify et Y Justify définissent le positionnement du bouton de balise d’action par rapport à ce point.</span><span class="sxs-lookup"><span data-stu-id="97ba2-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="97ba2-108">Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="97ba2-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97ba2-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="97ba2-109">Cell name:</span></span>  <br/> | <span data-ttu-id="97ba2-110">SmartTag.</span><span class="sxs-lookup"><span data-stu-id="97ba2-110">SmartTags.</span></span>  <span data-ttu-id="97ba2-111">*nom* . Y où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="97ba2-111">*name*  .Y           where SmartTags.</span></span> <span data-ttu-id="97ba2-112">*Name* est le nom de la ligne de balise d'action</span><span class="sxs-lookup"><span data-stu-id="97ba2-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="97ba2-113">Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="97ba2-113">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97ba2-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="97ba2-114">Section index:</span></span>  <br/> |<span data-ttu-id="97ba2-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="97ba2-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="97ba2-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="97ba2-116">Row index:</span></span>  <br/> |<span data-ttu-id="97ba2-117">**visRowSmartTag** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="97ba2-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="97ba2-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="97ba2-118">Cell index:</span></span>  <br/> |<span data-ttu-id="97ba2-119">**visSmartTagY**</span><span class="sxs-lookup"><span data-stu-id="97ba2-119">**visSmartTagY**</span></span> <br/> |
   

