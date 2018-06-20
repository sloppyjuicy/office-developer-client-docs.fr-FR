---
title: X, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: Le x - position des coordonnées dans le système de coordonnées locales de la forme autour de laquelle est positionné le bouton de balise d’action.
ms.openlocfilehash: f6b3a57b825c96398058e7b71e3cebeb8480dd49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790047"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="c446a-103">X, cellule (section Action Tags)</span><span class="sxs-lookup"><span data-stu-id="c446a-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="c446a-104">*X* -position dans les coordonnées locales de la forme autour de laquelle est positionné le bouton de balise d’action de la coordonnée.</span><span class="sxs-lookup"><span data-stu-id="c446a-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c446a-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="c446a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c446a-106">Notes</span><span class="sxs-lookup"><span data-stu-id="c446a-106">Remarks</span></span>

<span data-ttu-id="c446a-107">Les cellules X et Y définissent un point dans le système de coordonnées locales de la forme, tandis que les cellules X Justify et Y Justify définissent le positionnement du bouton de balise d’action par rapport à ce point.</span><span class="sxs-lookup"><span data-stu-id="c446a-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="c446a-108">Pour obtenir une référence à la cellule X par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c446a-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c446a-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c446a-109">Cell name:</span></span>  <br/> |<span data-ttu-id="c446a-110">Balises actives.</span><span class="sxs-lookup"><span data-stu-id="c446a-110">SmartTags.</span></span> <span data-ttu-id="c446a-111">*nom* . X où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="c446a-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="c446a-112">*nom* est le nom de la ligne de balise d’action</span><span class="sxs-lookup"><span data-stu-id="c446a-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="c446a-113">Pour obtenir une référence à la cellule X par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c446a-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c446a-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c446a-114">Section index:</span></span>  <br/> |<span data-ttu-id="c446a-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="c446a-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="c446a-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c446a-116">Row index:</span></span>  <br/> |<span data-ttu-id="c446a-117">**visRowSmartTag** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c446a-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c446a-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c446a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c446a-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="c446a-119">**visSmartTagX**</span></span> <br/> |
   

