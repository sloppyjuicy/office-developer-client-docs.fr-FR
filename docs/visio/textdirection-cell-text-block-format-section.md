---
title: TextDirection, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Détermine le sens des caractères dans un bloc de texte.
ms.openlocfilehash: c238b6b2a47c968809869f8eb3e38b6f0db1dcad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789890"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="8e811-103">TextDirection, cellule (section Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="8e811-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="8e811-104">Détermine le sens des caractères dans un bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="8e811-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="8e811-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8e811-105">**Value**</span></span>|<span data-ttu-id="8e811-106">**Direction**</span><span class="sxs-lookup"><span data-stu-id="8e811-106">**Direction**</span></span>|<span data-ttu-id="8e811-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="8e811-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8e811-108">0</span><span class="sxs-lookup"><span data-stu-id="8e811-108">0</span></span>  <br/> | <span data-ttu-id="8e811-109">Horizontal</span><span class="sxs-lookup"><span data-stu-id="8e811-109">Horizontal</span></span>  <br/> |<span data-ttu-id="8e811-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="8e811-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="8e811-111">1</span><span class="sxs-lookup"><span data-stu-id="8e811-111">1</span></span>  <br/> | <span data-ttu-id="8e811-112">Vertical</span><span class="sxs-lookup"><span data-stu-id="8e811-112">Vertical</span></span>  <br/> |<span data-ttu-id="8e811-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="8e811-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e811-114">Note</span><span class="sxs-lookup"><span data-stu-id="8e811-114">Remarks</span></span>

<span data-ttu-id="8e811-115">Dans la version japonaise 5.0 de Visio, la valeur de cette cellule était stockée dans la cellule VerticalText de la section Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="8e811-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="8e811-116">Pour obtenir une référence à la cellule TextDirection par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="8e811-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e811-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8e811-117">Cell name:</span></span>  <br/> | <span data-ttu-id="8e811-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="8e811-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="8e811-119">Pour obtenir une référence à la cellule TextDirection par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8e811-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e811-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8e811-120">Section index:</span></span>  <br/> |<span data-ttu-id="8e811-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8e811-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8e811-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8e811-122">Row index:</span></span>  <br/> |<span data-ttu-id="8e811-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="8e811-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="8e811-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8e811-124">Cell index:</span></span>  <br/> |<span data-ttu-id="8e811-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="8e811-125">**visTxtBlkDirection**</span></span> <br/> |
   

