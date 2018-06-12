---
title: VerticalAlign, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Détermine l'alignement vertical du texte dans le bloc de texte.
ms.openlocfilehash: cfd34f17eec597c306b69f76929877013b39015e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790014"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="888e8-103">VerticalAlign, cellule (section Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="888e8-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="888e8-104">Détermine l'alignement vertical du texte dans le bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="888e8-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="888e8-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="888e8-105">**Value**</span></span>|<span data-ttu-id="888e8-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="888e8-106">**Description**</span></span>|<span data-ttu-id="888e8-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="888e8-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="888e8-108">0</span><span class="sxs-lookup"><span data-stu-id="888e8-108">0</span></span>  <br/> | <span data-ttu-id="888e8-109">Haut</span><span class="sxs-lookup"><span data-stu-id="888e8-109">Top</span></span>  <br/> |<span data-ttu-id="888e8-110">**visVertTop**</span><span class="sxs-lookup"><span data-stu-id="888e8-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="888e8-111">1</span><span class="sxs-lookup"><span data-stu-id="888e8-111">1</span></span>  <br/> | <span data-ttu-id="888e8-112">Milieu</span><span class="sxs-lookup"><span data-stu-id="888e8-112">Middle</span></span>  <br/> |<span data-ttu-id="888e8-113">**visVertMiddle**</span><span class="sxs-lookup"><span data-stu-id="888e8-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="888e8-114">2</span><span class="sxs-lookup"><span data-stu-id="888e8-114">2</span></span>  <br/> | <span data-ttu-id="888e8-115">Bas</span><span class="sxs-lookup"><span data-stu-id="888e8-115">Bottom</span></span>  <br/> |<span data-ttu-id="888e8-116">**visVertBottom**</span><span class="sxs-lookup"><span data-stu-id="888e8-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="888e8-117">Note</span><span class="sxs-lookup"><span data-stu-id="888e8-117">Remarks</span></span>

<span data-ttu-id="888e8-118">Pour obtenir une référence à la cellule VerticalAlign par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="888e8-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="888e8-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="888e8-119">Cell name:</span></span>  <br/> | <span data-ttu-id="888e8-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="888e8-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="888e8-121">Pour obtenir une référence à la cellule VerticalAlign par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="888e8-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="888e8-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="888e8-122">Section index:</span></span>  <br/> |<span data-ttu-id="888e8-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="888e8-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="888e8-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="888e8-124">Row index:</span></span>  <br/> |<span data-ttu-id="888e8-125">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="888e8-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="888e8-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="888e8-126">Cell index:</span></span>  <br/> |<span data-ttu-id="888e8-127">**visTxtBlkVerticalAlign**</span><span class="sxs-lookup"><span data-stu-id="888e8-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

