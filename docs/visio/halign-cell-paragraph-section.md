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
ms.openlocfilehash: 224e495e8aea70c418a0ab7f5a7d56975d9868e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788762"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="035fd-103">HAlign, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="035fd-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="035fd-104">Détermine l'alignement horizontal du texte dans le bloc de texte de la forme.</span><span class="sxs-lookup"><span data-stu-id="035fd-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="035fd-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="035fd-105">**Value**</span></span>|<span data-ttu-id="035fd-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="035fd-106">**Description**</span></span>|<span data-ttu-id="035fd-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="035fd-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="035fd-108">0</span><span class="sxs-lookup"><span data-stu-id="035fd-108">0</span></span>  <br/> | <span data-ttu-id="035fd-109">Alignement à gauche</span><span class="sxs-lookup"><span data-stu-id="035fd-109">Left align</span></span>  <br/> |<span data-ttu-id="035fd-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="035fd-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="035fd-111">1</span><span class="sxs-lookup"><span data-stu-id="035fd-111">1</span></span>  <br/> | <span data-ttu-id="035fd-112">Au centre</span><span class="sxs-lookup"><span data-stu-id="035fd-112">Center</span></span>  <br/> |<span data-ttu-id="035fd-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="035fd-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="035fd-114">2</span><span class="sxs-lookup"><span data-stu-id="035fd-114">2</span></span>  <br/> | <span data-ttu-id="035fd-115">Alignement à droite</span><span class="sxs-lookup"><span data-stu-id="035fd-115">Right align</span></span>  <br/> |<span data-ttu-id="035fd-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="035fd-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="035fd-117">3</span><span class="sxs-lookup"><span data-stu-id="035fd-117">3</span></span>  <br/> | <span data-ttu-id="035fd-118">Justifié</span><span class="sxs-lookup"><span data-stu-id="035fd-118">Justify</span></span>  <br/> |<span data-ttu-id="035fd-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="035fd-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="035fd-120">4</span><span class="sxs-lookup"><span data-stu-id="035fd-120">4</span></span>  <br/> | <span data-ttu-id="035fd-121">Justification forcée</span><span class="sxs-lookup"><span data-stu-id="035fd-121">Force justify</span></span>  <br/> |<span data-ttu-id="035fd-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="035fd-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="035fd-123">Note</span><span class="sxs-lookup"><span data-stu-id="035fd-123">Remarks</span></span>

<span data-ttu-id="035fd-124">La justification ajoute des espaces entre les mots de toutes les lignes, à l'exception de la dernière ligne du paragraphe, pour aligner les côtés gauche et droit du texte sur les marges.</span><span class="sxs-lookup"><span data-stu-id="035fd-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="035fd-125">La justification forcée aligne toutes les lignes du paragraphe, y compris la dernière.</span><span class="sxs-lookup"><span data-stu-id="035fd-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="035fd-126">Pour obtenir une référence à la cellule HAlign par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="035fd-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="035fd-127">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="035fd-127">Cell name:</span></span>  <br/> | <span data-ttu-id="035fd-128">Para.HorzAlign [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="035fd-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="035fd-129">Pour obtenir une référence à la cellule HAlign par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="035fd-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="035fd-130">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="035fd-130">Section index:</span></span>  <br/> |<span data-ttu-id="035fd-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="035fd-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="035fd-132">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="035fd-132">Row index:</span></span>  <br/> |<span data-ttu-id="035fd-133">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="035fd-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="035fd-134">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="035fd-134">Cell index:</span></span>  <br/> |<span data-ttu-id="035fd-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="035fd-135">**visHorzAlign**</span></span> <br/> |
   

