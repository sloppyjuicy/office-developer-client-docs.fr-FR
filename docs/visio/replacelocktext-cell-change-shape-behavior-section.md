---
title: ReplaceLockText Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d'une forme remplacée pendant une opération de remplacement de forme. Le ReplaceLockText détermine si le texte affiché sur la forme de base remplace le texte de la forme remplacée.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348201"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="f0491-104">ReplaceLockText Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="f0491-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="f0491-105">Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d'une forme remplacée pendant une opération de remplacement de forme.</span><span class="sxs-lookup"><span data-stu-id="f0491-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="f0491-106">Le **ReplaceLockText** détermine si le texte affiché sur la forme de base remplace le texte de la forme remplacée.</span><span class="sxs-lookup"><span data-stu-id="f0491-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="f0491-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="f0491-107">**Value**</span></span>|<span data-ttu-id="f0491-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="f0491-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f0491-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="f0491-109">TRUE</span></span>  <br/> | <span data-ttu-id="f0491-110">Le texte de la forme de base remplace le texte de l'ancienne forme.</span><span class="sxs-lookup"><span data-stu-id="f0491-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="f0491-111">En outre, la forme de base remplace les valeurs des cellules dans les sections suivantes lors d'une opération de remplacement de forme:</span><span class="sxs-lookup"><span data-stu-id="f0491-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="f0491-112">Section **champs de texte**</span><span class="sxs-lookup"><span data-stu-id="f0491-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="f0491-113">Section **format de bloc de texte**</span><span class="sxs-lookup"><span data-stu-id="f0491-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="f0491-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="f0491-114">FALSE</span></span>  <br/> |<span data-ttu-id="f0491-115">La forme de remplacement contient du texte, des champs de texte ou d'autres propriétés de texte de l'ancienne forme qui ont été ajoutées à la forme.</span><span class="sxs-lookup"><span data-stu-id="f0491-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="f0491-116">Lorsque la forme de remplacement contient des propriétés de texte de l'ancienne forme, la forme de remplacement a également les valeurs des sections **character** et **paragraph** de l'ancienne forme s'il y a plus d'une ligne.</span><span class="sxs-lookup"><span data-stu-id="f0491-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="f0491-117">Si la valeur est définie sur TRUE (1), les valeurs de la forme de base remplacent les valeurs des éléments suivants sur la forme remplacée:</span><span class="sxs-lookup"><span data-stu-id="f0491-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="f0491-118">TheText, cellule (section Events)</span><span class="sxs-lookup"><span data-stu-id="f0491-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="f0491-119">Cellules dans la [section Character](character-section.md)</span><span class="sxs-lookup"><span data-stu-id="f0491-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="f0491-120">Cellules dans la [section Paragraph](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="f0491-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="f0491-121">Cellules de la [section onglets](tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="f0491-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0491-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0491-122">Remarks</span></span>

<span data-ttu-id="f0491-123">Pour obtenir une référence à la cellule **ReplaceLockText** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="f0491-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0491-124">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="f0491-124">Cell name:</span></span>  <br/> | <span data-ttu-id="f0491-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="f0491-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="f0491-126">Pour obtenir une référence à la cellule **ReplaceLockText** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="f0491-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0491-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f0491-127">Section index:</span></span>  <br/> |<span data-ttu-id="f0491-128">**Définis**</span><span class="sxs-lookup"><span data-stu-id="f0491-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f0491-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f0491-129">Row index:</span></span>  <br/> |<span data-ttu-id="f0491-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="f0491-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="f0491-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f0491-131">Cell index:</span></span>  <br/> |<span data-ttu-id="f0491-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="f0491-132">**visReplaceLockText**</span></span> <br/> |
   

