---
title: ReplaceLockText, cellule (Section de comportement de forme modification)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme. Le ReplaceLockText détermine si le texte affiché sur le contrôleur de remplace le texte de la forme remplacée.
ms.openlocfilehash: 75fb0831e7361345f04d7912eb0a55959d9417cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789481"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="c1ebf-104">ReplaceLockText, cellule (Section de comportement de forme modification)</span><span class="sxs-lookup"><span data-stu-id="c1ebf-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="c1ebf-105">Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme.</span><span class="sxs-lookup"><span data-stu-id="c1ebf-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="c1ebf-106">Le **ReplaceLockText** détermine si le texte affiché sur le contrôleur de remplace le texte de la forme remplacée.</span><span class="sxs-lookup"><span data-stu-id="c1ebf-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="c1ebf-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c1ebf-107">**Value**</span></span>|<span data-ttu-id="c1ebf-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="c1ebf-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1ebf-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="c1ebf-109">TRUE</span></span>  <br/> | <span data-ttu-id="c1ebf-110">Le texte de la forme de base remplace le texte de la forme ancien.</span><span class="sxs-lookup"><span data-stu-id="c1ebf-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="c1ebf-111">En outre, la forme de base remplace les valeurs des cellules dans les sections suivantes lors d’une opération de remplacement de forme :</span><span class="sxs-lookup"><span data-stu-id="c1ebf-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="c1ebf-112">Section **Champs de texte**</span><span class="sxs-lookup"><span data-stu-id="c1ebf-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="c1ebf-113">Section **Text Block Format**</span><span class="sxs-lookup"><span data-stu-id="c1ebf-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="c1ebf-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="c1ebf-114">FALSE</span></span>  <br/> |<span data-ttu-id="c1ebf-115">La forme de remplacement contient n’importe quel texte, les champs de texte ou autres propriétés de texte de la forme ancienne qui ont été ajoutées à la forme.</span><span class="sxs-lookup"><span data-stu-id="c1ebf-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="c1ebf-116">Lorsque la forme de remplacement contient les propriétés de texte de la forme ancienne, la forme de remplacement a également les valeurs dans les sections de **caractères** et de **paragraphes** de la forme ancienne s’ils disposent de plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="c1ebf-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="c1ebf-117">Si la valeur est TRUE (1), les valeurs de la forme principale remplace les valeurs des éléments suivants sur la forme remplacée :</span><span class="sxs-lookup"><span data-stu-id="c1ebf-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="c1ebf-118">TheText, cellule (section Events)</span><span class="sxs-lookup"><span data-stu-id="c1ebf-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="c1ebf-119">Cellules de la [Section Character](character-section.md)</span><span class="sxs-lookup"><span data-stu-id="c1ebf-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="c1ebf-120">Cellules dans la [Section Paragraph](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="c1ebf-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="c1ebf-121">Cellules dans la [Section Tabs](tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="c1ebf-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1ebf-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1ebf-122">Remarks</span></span>

<span data-ttu-id="c1ebf-123">Pour obtenir une référence à la cellule **ReplaceLockText** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c1ebf-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c1ebf-124">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c1ebf-124">Cell name:</span></span>  <br/> | <span data-ttu-id="c1ebf-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="c1ebf-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="c1ebf-126">Pour obtenir une référence à la cellule **ReplaceLockText** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c1ebf-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c1ebf-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c1ebf-127">Section index:</span></span>  <br/> |<span data-ttu-id="c1ebf-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c1ebf-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c1ebf-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c1ebf-129">Row index:</span></span>  <br/> |<span data-ttu-id="c1ebf-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="c1ebf-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="c1ebf-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c1ebf-131">Cell index:</span></span>  <br/> |<span data-ttu-id="c1ebf-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="c1ebf-132">**visReplaceLockText**</span></span> <br/> |
   

