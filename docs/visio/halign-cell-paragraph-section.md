---
title: HAlign, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Détermine l'alignement horizontal du texte dans le bloc de texte de la forme.
ms.openlocfilehash: a48619e2531c0a69ad63af3b88ae9f019019b1fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360178"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="d4c8a-103">HAlign, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="d4c8a-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="d4c8a-104">Détermine l'alignement horizontal du texte dans le bloc de texte de la forme.</span><span class="sxs-lookup"><span data-stu-id="d4c8a-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="d4c8a-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="d4c8a-105">**Value**</span></span>|<span data-ttu-id="d4c8a-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="d4c8a-106">**Description**</span></span>|<span data-ttu-id="d4c8a-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="d4c8a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d4c8a-108">0</span><span class="sxs-lookup"><span data-stu-id="d4c8a-108">0</span></span>  <br/> | <span data-ttu-id="d4c8a-109">Alignement à gauche</span><span class="sxs-lookup"><span data-stu-id="d4c8a-109">Left align</span></span>  <br/> |<span data-ttu-id="d4c8a-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="d4c8a-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="d4c8a-111">0,1</span><span class="sxs-lookup"><span data-stu-id="d4c8a-111">1</span></span>  <br/> | <span data-ttu-id="d4c8a-112">Centre</span><span class="sxs-lookup"><span data-stu-id="d4c8a-112">Center</span></span>  <br/> |<span data-ttu-id="d4c8a-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="d4c8a-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="d4c8a-114">n°2</span><span class="sxs-lookup"><span data-stu-id="d4c8a-114">2</span></span>  <br/> | <span data-ttu-id="d4c8a-115">Alignement à droite</span><span class="sxs-lookup"><span data-stu-id="d4c8a-115">Right align</span></span>  <br/> |<span data-ttu-id="d4c8a-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="d4c8a-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="d4c8a-117">3</span><span class="sxs-lookup"><span data-stu-id="d4c8a-117">3</span></span>  <br/> | <span data-ttu-id="d4c8a-118">Justifier</span><span class="sxs-lookup"><span data-stu-id="d4c8a-118">Justify</span></span>  <br/> |<span data-ttu-id="d4c8a-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="d4c8a-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="d4c8a-120">4</span><span class="sxs-lookup"><span data-stu-id="d4c8a-120">4</span></span>  <br/> | <span data-ttu-id="d4c8a-121">Justification forcée</span><span class="sxs-lookup"><span data-stu-id="d4c8a-121">Force justify</span></span>  <br/> |<span data-ttu-id="d4c8a-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="d4c8a-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4c8a-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="d4c8a-123">Remarks</span></span>

<span data-ttu-id="d4c8a-124">La justification ajoute des espaces entre les mots de toutes les lignes, à l'exception de la dernière ligne du paragraphe, pour aligner les côtés gauche et droit du texte sur les marges.</span><span class="sxs-lookup"><span data-stu-id="d4c8a-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="d4c8a-125">La justification forcée aligne toutes les lignes du paragraphe, y compris la dernière.</span><span class="sxs-lookup"><span data-stu-id="d4c8a-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="d4c8a-126">Pour obtenir une référence à la cellule HAlign par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d4c8a-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4c8a-127">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d4c8a-127">Cell name:</span></span>  <br/> | <span data-ttu-id="d4c8a-128">Para. HorzAlign [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d4c8a-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d4c8a-129">Pour obtenir une référence à la cellule HAlign à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d4c8a-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d4c8a-130">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d4c8a-130">Section index:</span></span>  <br/> |<span data-ttu-id="d4c8a-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="d4c8a-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="d4c8a-132">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d4c8a-132">Row index:</span></span>  <br/> |<span data-ttu-id="d4c8a-133">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d4c8a-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d4c8a-134">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d4c8a-134">Cell index:</span></span>  <br/> |<span data-ttu-id="d4c8a-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="d4c8a-135">**visHorzAlign**</span></span> <br/> |
   

