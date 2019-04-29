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
ms.openlocfilehash: 349bdc42485aa511011aeb85a43f1ab3e4ea853d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411427"
---
# <a name="style-cell-character-section"></a><span data-ttu-id="c3897-103">Style, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="c3897-103">Style Cell (Character Section)</span></span>

<span data-ttu-id="c3897-104">Présente la mise en forme de caractères appliquée à une plage de texte dans le bloc de texte de la forme.</span><span class="sxs-lookup"><span data-stu-id="c3897-104">Shows the character formatting applied to a range of text in the shape's text block.</span></span>
  
|<span data-ttu-id="c3897-105">**Style**</span><span class="sxs-lookup"><span data-stu-id="c3897-105">**Style**</span></span>|<span data-ttu-id="c3897-106">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c3897-106">**Value**</span></span>|<span data-ttu-id="c3897-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="c3897-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c3897-108">Gras</span><span class="sxs-lookup"><span data-stu-id="c3897-108">Bold</span></span>  <br/> | <span data-ttu-id="c3897-109">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="c3897-109">&amp;H1</span></span>  <br/> |<span data-ttu-id="c3897-110">**visBold**</span><span class="sxs-lookup"><span data-stu-id="c3897-110">**visBold**</span></span> <br/> |
| <span data-ttu-id="c3897-111">Italic</span><span class="sxs-lookup"><span data-stu-id="c3897-111">Italic</span></span>  <br/> | <span data-ttu-id="c3897-112">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="c3897-112">&amp;H2</span></span>  <br/> |<span data-ttu-id="c3897-113">**visItalic**</span><span class="sxs-lookup"><span data-stu-id="c3897-113">**visItalic**</span></span> <br/> |
| <span data-ttu-id="c3897-114">Underline</span><span class="sxs-lookup"><span data-stu-id="c3897-114">Underline</span></span>  <br/> | <span data-ttu-id="c3897-115">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="c3897-115">&amp;H4</span></span>  <br/> |<span data-ttu-id="c3897-116">**visUnderLine**</span><span class="sxs-lookup"><span data-stu-id="c3897-116">**visUnderLine**</span></span> <br/> |
| <span data-ttu-id="c3897-117">Petites majuscules</span><span class="sxs-lookup"><span data-stu-id="c3897-117">Small caps</span></span>  <br/> | <span data-ttu-id="c3897-118">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="c3897-118">&amp;H8</span></span>  <br/> |<span data-ttu-id="c3897-119">**visSmallCaps**</span><span class="sxs-lookup"><span data-stu-id="c3897-119">**visSmallCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c3897-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="c3897-120">Remarks</span></span>

<span data-ttu-id="c3897-p101">La cellule Style contient des informations de mise en forme qui sont appliquées à une sous-plage du texte d'une forme si la section Caractère contient plusieurs lignes. Dans le cas contraire, elle contient des informations de mise en forme pour la totalité du texte de la forme.</span><span class="sxs-lookup"><span data-stu-id="c3897-p101">The Style cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="c3897-123">La valeur représente un nombre binaire dans lequel chaque bit indique un style de caractères.</span><span class="sxs-lookup"><span data-stu-id="c3897-123">The value represents a binary number in which each bit indicates a character style.</span></span> <span data-ttu-id="c3897-124">Par exemple, une valeur de 3 indique que le texte est mis en forme à la fois en gras et en italique.</span><span class="sxs-lookup"><span data-stu-id="c3897-124">For example, a value of 3 represents text formatted in both italic and bold.</span></span> <span data-ttu-id="c3897-125">Si la valeur de Style est 0, le texte est normal, sans mise en forme.</span><span class="sxs-lookup"><span data-stu-id="c3897-125">If the value of Style is 0, the text is plain, or unformatted.</span></span> <span data-ttu-id="c3897-126">Vous pouvez tester un format particulier à l'aide de\* fonctions binaires booléennes.</span><span class="sxs-lookup"><span data-stu-id="c3897-126">You can test for a particular format using Boolean BIT\* functions.</span></span> <span data-ttu-id="c3897-127">Pour plus de précisions sur ces fonctions, reportez-vous à votre documentation de programmation.</span><span class="sxs-lookup"><span data-stu-id="c3897-127">See your programming documentation for details about these functions.</span></span>
  
<span data-ttu-id="c3897-128">Pour obtenir une référence à la cellule Style par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="c3897-128">To get a reference to the Style cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c3897-129">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c3897-129">Cell name:</span></span>  <br/> | <span data-ttu-id="c3897-130">Char. style [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c3897-130">Char.Style[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c3897-131">Pour obtenir une référence à la cellule Style par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c3897-131">To get a reference to the Style cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c3897-132">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c3897-132">Section index:</span></span>  <br/> |<span data-ttu-id="c3897-133">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="c3897-133">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="c3897-134">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c3897-134">Row index:</span></span>  <br/> |<span data-ttu-id="c3897-135">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c3897-135">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c3897-136">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c3897-136">Cell index:</span></span>  <br/> |<span data-ttu-id="c3897-137">**visCharacterStyle**</span><span class="sxs-lookup"><span data-stu-id="c3897-137">**visCharacterStyle**</span></span> <br/> |
   
 <span data-ttu-id="c3897-138">*Exemple*</span><span class="sxs-lookup"><span data-stu-id="c3897-138">*Example*</span></span> 
  
<span data-ttu-id="c3897-139">Supposons que la cellule Color de la première ligne de la section Character d'une forme soit définie par la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="c3897-139">Suppose the Color cell in the first row of a shape's Character section is set to this formula:</span></span>
  
<span data-ttu-id="c3897-140">= IF (BITAND (Char. style, 1) = 1, 4, 3)</span><span class="sxs-lookup"><span data-stu-id="c3897-140">= IF(BITAND(Char.Style,1)=1,4,3)</span></span>
  
<span data-ttu-id="c3897-p103">Si le premier caractère du texte de la forme est mis en gras, le texte couvert par la première ligne de propriétés Character est bleu (4) ; sinon, il est vert (3). Cet exemple part du principe que les couleurs par défaut sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="c3897-p103">Then if the first character of the shape's text is bold, the text covered by the first Character properties row will be blue (4); otherwise it will be green (3). This example assumes default colors are in effect.</span></span>
  
<span data-ttu-id="c3897-p104">La formule suivante est un exemple de définition de la cellule Style dans un programme. La première instruction fait référence à la cellule Style par son nom et la deuxième, par index. Les deux instructions permettent d'appliquer l'italique au texte couvert par la deuxième ligne de la section Character d'une forme.</span><span class="sxs-lookup"><span data-stu-id="c3897-p104">The following is an example of setting the Style cell in a program. The first statement references the Style cell by name, and the second statement references the Style cell by index. Both statements apply italic to the text covered by the second row of a shape's Character section.</span></span>
  

