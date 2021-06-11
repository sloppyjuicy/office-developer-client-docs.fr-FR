---
title: X Justify, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: Décalage x du bouton de balise d’action par rapport au point défini par les cellules X et Y.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414122"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="4ea54-103">X Justify Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="4ea54-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="4ea54-104">Décalage  *x*  du bouton de balise d’action par rapport au point défini par les cellules X et Y.</span><span class="sxs-lookup"><span data-stu-id="4ea54-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4ea54-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="4ea54-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="4ea54-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4ea54-106">**Value**</span></span>|<span data-ttu-id="4ea54-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="4ea54-107">**Description**</span></span>|<span data-ttu-id="4ea54-108">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="4ea54-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4ea54-109">0</span><span class="sxs-lookup"><span data-stu-id="4ea54-109">0</span></span>  <br/> | <span data-ttu-id="4ea54-110">Aligné à gauche (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="4ea54-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="4ea54-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="4ea54-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="4ea54-112">1</span><span class="sxs-lookup"><span data-stu-id="4ea54-112">1</span></span>  <br/> | <span data-ttu-id="4ea54-113">Centré.</span><span class="sxs-lookup"><span data-stu-id="4ea54-113">Centered.</span></span>  <br/> |<span data-ttu-id="4ea54-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="4ea54-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="4ea54-115">2</span><span class="sxs-lookup"><span data-stu-id="4ea54-115">2</span></span>  <br/> | <span data-ttu-id="4ea54-116">Aligné à droite.</span><span class="sxs-lookup"><span data-stu-id="4ea54-116">Right justified.</span></span>  <br/> |<span data-ttu-id="4ea54-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="4ea54-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ea54-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="4ea54-118">Remarks</span></span>

<span data-ttu-id="4ea54-119">Les cellules X Justify et Y Justify déterminent où le bouton de balise d’action est placé par rapport au point défini dans les cellules X et Y.</span><span class="sxs-lookup"><span data-stu-id="4ea54-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="4ea54-120">Pour obtenir une référence à la cellule X Justify à partir du nom d’une autre formule ou d’un programme à partir de la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="4ea54-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4ea54-121">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="4ea54-121">Cell name:</span></span>  <br/> | <span data-ttu-id="4ea54-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="4ea54-122">SmartTags.</span></span>  <span data-ttu-id="4ea54-123">*nom*  . XJustify où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="4ea54-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="4ea54-124">*name est*  le nom de la ligne de balise d’action</span><span class="sxs-lookup"><span data-stu-id="4ea54-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="4ea54-125">Pour obtenir une référence à la cellule X Justify par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="4ea54-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4ea54-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="4ea54-126">Section index:</span></span>  <br/> |<span data-ttu-id="4ea54-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="4ea54-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="4ea54-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="4ea54-128">Row index:</span></span>  <br/> |<span data-ttu-id="4ea54-129">**visRowSmartTag**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4ea54-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4ea54-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4ea54-130">Cell index:</span></span>  <br/> |<span data-ttu-id="4ea54-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="4ea54-131">**visSmartTagXJustify**</span></span> <br/> |
   

