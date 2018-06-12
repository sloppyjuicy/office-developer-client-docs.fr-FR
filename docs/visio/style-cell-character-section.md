---
title: Style, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Présente la mise en forme de caractères appliquée à une plage de texte dans le bloc de texte de la forme.
ms.openlocfilehash: 48bda5eb798f439e2616b2b910d7ec5ac719d060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789815"
---
# <a name="style-cell-character-section"></a><span data-ttu-id="c2430-103">Style, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="c2430-103">Style Cell (Character Section)</span></span>

<span data-ttu-id="c2430-104">Présente la mise en forme de caractères appliquée à une plage de texte dans le bloc de texte de la forme.</span><span class="sxs-lookup"><span data-stu-id="c2430-104">Shows the character formatting applied to a range of text in the shape's text block.</span></span>
  
|<span data-ttu-id="c2430-105">**Style**</span><span class="sxs-lookup"><span data-stu-id="c2430-105">**Style**</span></span>|<span data-ttu-id="c2430-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c2430-106">**Value**</span></span>|<span data-ttu-id="c2430-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="c2430-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c2430-108">Gras</span><span class="sxs-lookup"><span data-stu-id="c2430-108">Bold</span></span>  <br/> | <span data-ttu-id="c2430-109">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="c2430-109">&amp;H1</span></span>  <br/> |<span data-ttu-id="c2430-110">**visBold**</span><span class="sxs-lookup"><span data-stu-id="c2430-110">**visBold**</span></span> <br/> |
| <span data-ttu-id="c2430-111">Italique</span><span class="sxs-lookup"><span data-stu-id="c2430-111">Italic</span></span>  <br/> | <span data-ttu-id="c2430-112">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="c2430-112">&amp;H2</span></span>  <br/> |<span data-ttu-id="c2430-113">**visItalic**</span><span class="sxs-lookup"><span data-stu-id="c2430-113">**visItalic**</span></span> <br/> |
| <span data-ttu-id="c2430-114">Souligné</span><span class="sxs-lookup"><span data-stu-id="c2430-114">Underline</span></span>  <br/> | <span data-ttu-id="c2430-115">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="c2430-115">&amp;H4</span></span>  <br/> |<span data-ttu-id="c2430-116">**visUnderLine**</span><span class="sxs-lookup"><span data-stu-id="c2430-116">**visUnderLine**</span></span> <br/> |
| <span data-ttu-id="c2430-117">Petites majuscules</span><span class="sxs-lookup"><span data-stu-id="c2430-117">Small caps</span></span>  <br/> | <span data-ttu-id="c2430-118">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="c2430-118">&amp;H8</span></span>  <br/> |<span data-ttu-id="c2430-119">**visSmallCaps**</span><span class="sxs-lookup"><span data-stu-id="c2430-119">**visSmallCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2430-120">Note</span><span class="sxs-lookup"><span data-stu-id="c2430-120">Remarks</span></span>

<span data-ttu-id="c2430-p101">La cellule Style contient des informations de mise en forme qui sont appliquées à une sous-plage du texte d'une forme si la section Caractère contient plusieurs lignes. Dans le cas contraire, elle contient des informations de mise en forme pour la totalité du texte de la forme.</span><span class="sxs-lookup"><span data-stu-id="c2430-p101">The Style cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="c2430-123">La valeur représente un nombre binaire dans lequel chaque bit indique un style de caractère.</span><span class="sxs-lookup"><span data-stu-id="c2430-123">The value represents a binary number in which each bit indicates a character style.</span></span> <span data-ttu-id="c2430-124">Par exemple, une valeur de 3 représente texte mis en forme en gras et en italique.</span><span class="sxs-lookup"><span data-stu-id="c2430-124">For example, a value of 3 represents text formatted in both italic and bold.</span></span> <span data-ttu-id="c2430-125">Si la valeur du Style est 0, le texte est normal, sans mise en forme.</span><span class="sxs-lookup"><span data-stu-id="c2430-125">If the value of Style is 0, the text is plain, or unformatted.</span></span> <span data-ttu-id="c2430-126">Vous pouvez tester un format spécifique à l’aide de bits Boolean\* fonctions.</span><span class="sxs-lookup"><span data-stu-id="c2430-126">You can test for a particular format using Boolean BIT\* functions.</span></span> <span data-ttu-id="c2430-127">Reportez-vous à la documentation pour plus d’informations sur ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="c2430-127">See your programming documentation for details about these functions.</span></span>
  
<span data-ttu-id="c2430-128">Pour obtenir une référence à la cellule Style par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c2430-128">To get a reference to the Style cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2430-129">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c2430-129">Cell name:</span></span>  <br/> | <span data-ttu-id="c2430-130">Char.Style [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c2430-130">Char.Style[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c2430-131">Pour obtenir une référence à la cellule Style par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c2430-131">To get a reference to the Style cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2430-132">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c2430-132">Section index:</span></span>  <br/> |<span data-ttu-id="c2430-133">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="c2430-133">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="c2430-134">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c2430-134">Row index:</span></span>  <br/> |<span data-ttu-id="c2430-135">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c2430-135">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c2430-136">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c2430-136">Cell index:</span></span>  <br/> |<span data-ttu-id="c2430-137">**visCharacterStyle**</span><span class="sxs-lookup"><span data-stu-id="c2430-137">**visCharacterStyle**</span></span> <br/> |
   
 <span data-ttu-id="c2430-138">*Exemple*</span><span class="sxs-lookup"><span data-stu-id="c2430-138">*Example*</span></span> 
  
<span data-ttu-id="c2430-139">Supposons que la cellule Color de la première ligne de la section Character d'une forme soit définie par la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="c2430-139">Suppose the Color cell in the first row of a shape's Character section is set to this formula:</span></span>
  
<span data-ttu-id="c2430-140">= IF(BITAND(Char.Style,1)=1,4,3)</span><span class="sxs-lookup"><span data-stu-id="c2430-140">= IF(BITAND(Char.Style,1)=1,4,3)</span></span>
  
<span data-ttu-id="c2430-p103">Si le premier caractère du texte de la forme est mis en gras, le texte couvert par la première ligne de propriétés Character est bleu (4) ; sinon, il est vert (3). Cet exemple part du principe que les couleurs par défaut sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="c2430-p103">Then if the first character of the shape's text is bold, the text covered by the first Character properties row will be blue (4); otherwise it will be green (3). This example assumes default colors are in effect.</span></span>
  
<span data-ttu-id="c2430-p104">La formule suivante est un exemple de définition de la cellule Style dans un programme. La première instruction fait référence à la cellule Style par son nom et la deuxième, par index. Les deux instructions permettent d'appliquer l'italique au texte couvert par la deuxième ligne de la section Character d'une forme.</span><span class="sxs-lookup"><span data-stu-id="c2430-p104">The following is an example of setting the Style cell in a program. The first statement references the Style cell by name, and the second statement references the Style cell by index. Both statements apply italic to the text covered by the second row of a shape's Character section.</span></span>
  

