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
description: Position de la coordonnée x dans les coordonnées locales de la forme et entourant laquelle se trouve le bouton de balise d'action.
ms.openlocfilehash: 9f26bec81563c9813a88ed5c69730266834ee101
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431112"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="40905-103">X, cellule (section Action Tags)</span><span class="sxs-lookup"><span data-stu-id="40905-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="40905-104">Position de la coordonnée *x* dans les coordonnées locales de la forme et entourant laquelle se trouve le bouton de balise d'action.</span><span class="sxs-lookup"><span data-stu-id="40905-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="40905-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="40905-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="40905-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="40905-106">Remarks</span></span>

<span data-ttu-id="40905-107">Les cellules X et Y définissent un point dans le système de coordonnées locales de la forme, tandis que les cellules X Justify et Y Justify définissent le positionnement du bouton de balise d’action par rapport à ce point.</span><span class="sxs-lookup"><span data-stu-id="40905-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="40905-108">Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="40905-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40905-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="40905-109">Cell name:</span></span>  <br/> |<span data-ttu-id="40905-110">SmartTag.</span><span class="sxs-lookup"><span data-stu-id="40905-110">SmartTags.</span></span> <span data-ttu-id="40905-111">*nom* . X où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="40905-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="40905-112">*Name* est le nom de la ligne de balise d'action</span><span class="sxs-lookup"><span data-stu-id="40905-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="40905-113">Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="40905-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40905-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="40905-114">Section index:</span></span>  <br/> |<span data-ttu-id="40905-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="40905-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="40905-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="40905-116">Row index:</span></span>  <br/> |<span data-ttu-id="40905-117">**visRowSmartTag** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="40905-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="40905-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="40905-118">Cell index:</span></span>  <br/> |<span data-ttu-id="40905-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="40905-119">**visSmartTagX**</span></span> <br/> |
   

