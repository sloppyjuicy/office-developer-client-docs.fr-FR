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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414738"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="09703-103">HAlign, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="09703-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="09703-104">Détermine l'alignement horizontal du texte dans le bloc de texte de la forme.</span><span class="sxs-lookup"><span data-stu-id="09703-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="09703-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="09703-105">**Value**</span></span>|<span data-ttu-id="09703-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="09703-106">**Description**</span></span>|<span data-ttu-id="09703-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="09703-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="09703-108">0</span><span class="sxs-lookup"><span data-stu-id="09703-108">0</span></span>  <br/> | <span data-ttu-id="09703-109">Alignement à gauche</span><span class="sxs-lookup"><span data-stu-id="09703-109">Left align</span></span>  <br/> |<span data-ttu-id="09703-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="09703-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="09703-111">0,1</span><span class="sxs-lookup"><span data-stu-id="09703-111">1</span></span>  <br/> | <span data-ttu-id="09703-112">Centre</span><span class="sxs-lookup"><span data-stu-id="09703-112">Center</span></span>  <br/> |<span data-ttu-id="09703-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="09703-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="09703-114">n°2</span><span class="sxs-lookup"><span data-stu-id="09703-114">2</span></span>  <br/> | <span data-ttu-id="09703-115">Alignement à droite</span><span class="sxs-lookup"><span data-stu-id="09703-115">Right align</span></span>  <br/> |<span data-ttu-id="09703-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="09703-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="09703-117">3</span><span class="sxs-lookup"><span data-stu-id="09703-117">3</span></span>  <br/> | <span data-ttu-id="09703-118">Justifier</span><span class="sxs-lookup"><span data-stu-id="09703-118">Justify</span></span>  <br/> |<span data-ttu-id="09703-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="09703-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="09703-120">4</span><span class="sxs-lookup"><span data-stu-id="09703-120">4</span></span>  <br/> | <span data-ttu-id="09703-121">Justification forcée</span><span class="sxs-lookup"><span data-stu-id="09703-121">Force justify</span></span>  <br/> |<span data-ttu-id="09703-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="09703-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09703-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="09703-123">Remarks</span></span>

<span data-ttu-id="09703-124">La justification ajoute des espaces entre les mots de toutes les lignes, à l'exception de la dernière ligne du paragraphe, pour aligner les côtés gauche et droit du texte sur les marges.</span><span class="sxs-lookup"><span data-stu-id="09703-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="09703-125">La justification forcée aligne toutes les lignes du paragraphe, y compris la dernière.</span><span class="sxs-lookup"><span data-stu-id="09703-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="09703-126">Pour obtenir une référence à la cellule HAlign par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="09703-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09703-127">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="09703-127">Cell name:</span></span>  <br/> | <span data-ttu-id="09703-128">Para. HorzAlign [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="09703-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="09703-129">Pour obtenir une référence à la cellule HAlign à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="09703-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09703-130">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="09703-130">Section index:</span></span>  <br/> |<span data-ttu-id="09703-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="09703-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="09703-132">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="09703-132">Row index:</span></span>  <br/> |<span data-ttu-id="09703-133">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="09703-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="09703-134">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="09703-134">Cell index:</span></span>  <br/> |<span data-ttu-id="09703-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="09703-135">**visHorzAlign**</span></span> <br/> |
   

