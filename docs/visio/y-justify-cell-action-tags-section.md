---
title: Y Justify, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Décalage y du bouton de balise d’action par rapport au point défini par les cellules X et Y.
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419981"
---
# <a name="y-justify-cell-action-tags-section"></a><span data-ttu-id="1d1e1-103">Y Justify, cellule (section Action Tags)</span><span class="sxs-lookup"><span data-stu-id="1d1e1-103">Y Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="1d1e1-104">Décalage  *y*  du bouton de balise d’action par rapport au point défini par les cellules X et Y.</span><span class="sxs-lookup"><span data-stu-id="1d1e1-104">The  *y*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1d1e1-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="1d1e1-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="1d1e1-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="1d1e1-106">**Value**</span></span>|<span data-ttu-id="1d1e1-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="1d1e1-107">**Description**</span></span>|<span data-ttu-id="1d1e1-108">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="1d1e1-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1d1e1-109">0</span><span class="sxs-lookup"><span data-stu-id="1d1e1-109">0</span></span>  <br/> | <span data-ttu-id="1d1e1-110">Aligné en haut (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="1d1e1-110">Top justified (the default).</span></span>  <br/> |<span data-ttu-id="1d1e1-111">**visSmartTagYJustifyTop**</span><span class="sxs-lookup"><span data-stu-id="1d1e1-111">**visSmartTagYJustifyTop**</span></span> <br/> |
| <span data-ttu-id="1d1e1-112">1 </span><span class="sxs-lookup"><span data-stu-id="1d1e1-112">1</span></span>  <br/> | <span data-ttu-id="1d1e1-113">Centré.</span><span class="sxs-lookup"><span data-stu-id="1d1e1-113">Centered.</span></span>  <br/> |<span data-ttu-id="1d1e1-114">**visSmartTagYJustifyMiddle**</span><span class="sxs-lookup"><span data-stu-id="1d1e1-114">**visSmartTagYJustifyMiddle**</span></span> <br/> |
| <span data-ttu-id="1d1e1-115">2 </span><span class="sxs-lookup"><span data-stu-id="1d1e1-115">2</span></span>  <br/> | <span data-ttu-id="1d1e1-116">Aligné en bas.</span><span class="sxs-lookup"><span data-stu-id="1d1e1-116">Bottom justified.</span></span>  <br/> |<span data-ttu-id="1d1e1-117">**visSmartTagYJustifyBottom**</span><span class="sxs-lookup"><span data-stu-id="1d1e1-117">**visSmartTagYJustifyBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d1e1-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d1e1-118">Remarks</span></span>

<span data-ttu-id="1d1e1-119">Les cellules X Justify et Y Justify déterminent où le bouton de balise d’action est placé par rapport au point défini dans les cellules X et Y.</span><span class="sxs-lookup"><span data-stu-id="1d1e1-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span>
  
<span data-ttu-id="1d1e1-120">Pour obtenir une référence à la cellule Y Justify par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="1d1e1-120">To get a reference to the Y Justify cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1d1e1-121">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="1d1e1-121">Cell name:</span></span>  <br/> | <span data-ttu-id="1d1e1-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="1d1e1-122">SmartTags.</span></span>  <span data-ttu-id="1d1e1-123">*nom*  . YJustify où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="1d1e1-123">*name*  .YJustify           where SmartTags.</span></span> <span data-ttu-id="1d1e1-124">*name est*  le nom de la ligne de balise d’action</span><span class="sxs-lookup"><span data-stu-id="1d1e1-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="1d1e1-125">Pour obtenir une référence à la cellule Y Justify par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1d1e1-125">To get a reference to the Y Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1d1e1-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1d1e1-126">Section index:</span></span>  <br/> |<span data-ttu-id="1d1e1-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="1d1e1-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="1d1e1-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1d1e1-128">Row index:</span></span>  <br/> |<span data-ttu-id="1d1e1-129">**visRowSmartTag**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1d1e1-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1d1e1-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1d1e1-130">Cell index:</span></span>  <br/> |<span data-ttu-id="1d1e1-131">**visSmartTagYJustify**</span><span class="sxs-lookup"><span data-stu-id="1d1e1-131">**visSmartTagYJustify**</span></span> <br/> |
   

