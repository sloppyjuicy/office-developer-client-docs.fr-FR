---
title: ReplaceLockFormat, cellule (Section de comportement de forme modification)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme. Si la cellule ReplaceLockFormat d’une forme de base est définie sur TRUE (1), les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes de la forme remplacée par la forme de base.
ms.openlocfilehash: bf1e28353cc1e2d737a7d7a6dcd90caf14e19dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789448"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="02392-104">ReplaceLockFormat, cellule (Section de comportement de forme modification)</span><span class="sxs-lookup"><span data-stu-id="02392-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="02392-105">Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme.</span><span class="sxs-lookup"><span data-stu-id="02392-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="02392-106">Si la cellule **ReplaceLockFormat** d’une forme de base est définie sur TRUE (1), les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes de la forme remplacée par la forme de base.</span><span class="sxs-lookup"><span data-stu-id="02392-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="02392-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="02392-107">**Value**</span></span>|<span data-ttu-id="02392-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="02392-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02392-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="02392-109">TRUE</span></span>  <br/> |<span data-ttu-id="02392-110">Si la cellule **ReplaceLockFormat** d’une forme de base est définie sur TRUE, les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes de la forme remplacée par la forme de base.</span><span class="sxs-lookup"><span data-stu-id="02392-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="02392-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="02392-111">FALSE</span></span>  <br/> |<span data-ttu-id="02392-112">Si la cellule **ReplaceLockFormat** d’une forme de base est définie sur FALSE, la forme de remplacement contient les valeurs de mise en forme locales à partir de la forme ancienne après l’opération de remplacement.</span><span class="sxs-lookup"><span data-stu-id="02392-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02392-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="02392-113">Remarks</span></span>

<span data-ttu-id="02392-114">La cellule **ReplaceLockFormat** détermine si la forme de base remplace les valeurs locales de mise en forme des cellules dans les sections suivantes lors d’une opération de remplacement de forme :</span><span class="sxs-lookup"><span data-stu-id="02392-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="02392-115">Section **Format de remplissage**</span><span class="sxs-lookup"><span data-stu-id="02392-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="02392-116">Section **Format de ligne**</span><span class="sxs-lookup"><span data-stu-id="02392-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="02392-117">Section **Style rapide**</span><span class="sxs-lookup"><span data-stu-id="02392-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="02392-118">Section **Propriétés de thème**</span><span class="sxs-lookup"><span data-stu-id="02392-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="02392-119">Section **Propriétés du dégradé**</span><span class="sxs-lookup"><span data-stu-id="02392-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="02392-120">Section **Propriétés de biseau**</span><span class="sxs-lookup"><span data-stu-id="02392-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="02392-121">Section **Propriétés d’effet supplémentaires**</span><span class="sxs-lookup"><span data-stu-id="02392-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="02392-122">Section **Points de dégradés ligne**</span><span class="sxs-lookup"><span data-stu-id="02392-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="02392-123">Section **De dégradé de remplissage**</span><span class="sxs-lookup"><span data-stu-id="02392-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="02392-124">Pour obtenir une référence à la cellule **ReplaceLockFormat** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="02392-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02392-125">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="02392-125">Cell name:</span></span>  <br/> | <span data-ttu-id="02392-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="02392-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="02392-127">Pour obtenir une référence à la cellule **ReplaceLockFormat** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="02392-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02392-128">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="02392-128">Section index:</span></span>  <br/> |<span data-ttu-id="02392-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="02392-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="02392-130">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="02392-130">Row index:</span></span>  <br/> |<span data-ttu-id="02392-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="02392-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="02392-132">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="02392-132">Cell index:</span></span>  <br/> |<span data-ttu-id="02392-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="02392-133">**visReplaceLockFormat**</span></span> <br/> |
   

