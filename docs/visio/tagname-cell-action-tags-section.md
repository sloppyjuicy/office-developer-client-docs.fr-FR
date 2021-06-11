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
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417909"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="3bf94-103">TagName, cellule (section Action Tags)</span><span class="sxs-lookup"><span data-stu-id="3bf94-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="3bf94-104">Nom de la balise d’action utilisé comme référence pour associer la balise d’action à ses actions.</span><span class="sxs-lookup"><span data-stu-id="3bf94-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3bf94-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="3bf94-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3bf94-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="3bf94-106">Remarks</span></span>

 <span data-ttu-id="3bf94-107">La cellule TagName de la section Action Tags fonctionne avec la cellule TagName de la section Actions pour associer une balise d’action à ses actions.</span><span class="sxs-lookup"><span data-stu-id="3bf94-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="3bf94-108">Les lignes de la section Actions ont également une cellule TagName, et ces lignes avec la même valeur de cellule TagName que cette cellule définissent les actions à prendre pour cette balise d’action.</span><span class="sxs-lookup"><span data-stu-id="3bf94-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="3bf94-109">Pour obtenir une référence à la cellule TagName à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="3bf94-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3bf94-110">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="3bf94-110">Cell name:</span></span>  <br/> | <span data-ttu-id="3bf94-111">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="3bf94-111">SmartTags.</span></span>  <span data-ttu-id="3bf94-112">*nom*  . TagName où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="3bf94-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="3bf94-113">*name est*  le nom de la ligne de balise d’action</span><span class="sxs-lookup"><span data-stu-id="3bf94-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="3bf94-114">Pour obtenir une référence à la cellule TagName par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3bf94-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3bf94-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="3bf94-115">Section index:</span></span>  <br/> |<span data-ttu-id="3bf94-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="3bf94-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="3bf94-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="3bf94-117">Row index:</span></span>  <br/> |<span data-ttu-id="3bf94-118">**visRowSmartTag**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3bf94-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3bf94-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3bf94-119">Cell index:</span></span>  <br/> |<span data-ttu-id="3bf94-120">**visSmartTagName**</span><span class="sxs-lookup"><span data-stu-id="3bf94-120">**visSmartTagName**</span></span> <br/> |
   

