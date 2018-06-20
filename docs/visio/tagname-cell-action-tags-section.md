---
title: TagName, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Nom de la balise d’action utilisé comme référence pour associer la balise d’action à ses actions.
ms.openlocfilehash: dbac3d4dff9d2ffd18bba75db56cafc08f5e0ee8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789849"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="bc834-103">TagName, cellule (section Action Tags)</span><span class="sxs-lookup"><span data-stu-id="bc834-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="bc834-104">Nom de la balise d’action utilisé comme référence pour associer la balise d’action à ses actions.</span><span class="sxs-lookup"><span data-stu-id="bc834-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bc834-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="bc834-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bc834-106">Notes</span><span class="sxs-lookup"><span data-stu-id="bc834-106">Remarks</span></span>

 <span data-ttu-id="bc834-107">La cellule TagName de la section Action Tags fonctionne avec la cellule TagName de la section Actions pour associer une balise d’action à ses actions.</span><span class="sxs-lookup"><span data-stu-id="bc834-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="bc834-108">Lignes dans la section Actions ont également une cellule TagName, et les lignes avec la même valeur de cellule TagName en tant que cette cellule définissent les actions à effectuer pour cette balise d’action.</span><span class="sxs-lookup"><span data-stu-id="bc834-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="bc834-109">Pour obtenir une référence à la cellule TagName par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="bc834-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc834-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bc834-110">Cell name:</span></span>  <br/> | <span data-ttu-id="bc834-111">Balises actives.</span><span class="sxs-lookup"><span data-stu-id="bc834-111">SmartTags.</span></span>  <span data-ttu-id="bc834-112">*nom* . TagName où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="bc834-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="bc834-113">*nom* est le nom de la ligne de balise d’action</span><span class="sxs-lookup"><span data-stu-id="bc834-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="bc834-114">Pour obtenir une référence à la cellule TagName par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bc834-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc834-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bc834-115">Section index:</span></span>  <br/> |<span data-ttu-id="bc834-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="bc834-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="bc834-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bc834-117">Row index:</span></span>  <br/> |<span data-ttu-id="bc834-118">**visRowSmartTag** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bc834-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bc834-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bc834-119">Cell index:</span></span>  <br/> |<span data-ttu-id="bc834-120">**visSmartTagName**</span><span class="sxs-lookup"><span data-stu-id="bc834-120">**visSmartTagName**</span></span> <br/> |
   

