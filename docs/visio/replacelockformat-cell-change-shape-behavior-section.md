---
title: ReplaceLockFormat Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d'une forme remplacée pendant une opération de remplacement de forme. Si la cellule ReplaceLockFormat d'une forme de base est définie sur TRUE (1), les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes d'une forme remplacée par la forme de base.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329889"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="b8998-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="b8998-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="b8998-105">Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d'une forme remplacée pendant une opération de remplacement de forme.</span><span class="sxs-lookup"><span data-stu-id="b8998-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="b8998-106">Si la cellule **ReplaceLockFormat** d'une forme de base est définie sur true (1), les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes d'une forme remplacée par la forme de base.</span><span class="sxs-lookup"><span data-stu-id="b8998-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="b8998-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="b8998-107">**Value**</span></span>|<span data-ttu-id="b8998-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8998-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b8998-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="b8998-109">TRUE</span></span>  <br/> |<span data-ttu-id="b8998-110">Si la cellule **ReplaceLockFormat** d'une forme de base est définie sur true, les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes d'une forme remplacée par la forme de base.</span><span class="sxs-lookup"><span data-stu-id="b8998-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="b8998-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="b8998-111">FALSE</span></span>  <br/> |<span data-ttu-id="b8998-112">Si la cellule **ReplaceLockFormat** d'une forme de base est définie sur false, la forme de remplacement contient les valeurs de mise en forme locale de l'ancienne forme après l'opération de remplacement.</span><span class="sxs-lookup"><span data-stu-id="b8998-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8998-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8998-113">Remarks</span></span>

<span data-ttu-id="b8998-114">La cellule **ReplaceLockFormat** détermine si la forme de base remplace les valeurs de mise en forme locale des cellules dans les sections suivantes lors d'une opération de remplacement de forme:</span><span class="sxs-lookup"><span data-stu-id="b8998-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="b8998-115">Section **format de remplissage**</span><span class="sxs-lookup"><span data-stu-id="b8998-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="b8998-116">Section **format de ligne**</span><span class="sxs-lookup"><span data-stu-id="b8998-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="b8998-117">Section **style rapide**</span><span class="sxs-lookup"><span data-stu-id="b8998-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="b8998-118">Section **Propriétés du thème**</span><span class="sxs-lookup"><span data-stu-id="b8998-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="b8998-119">Section **Propriétés du dégradé**</span><span class="sxs-lookup"><span data-stu-id="b8998-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="b8998-120">Section **Propriétés du biseau**</span><span class="sxs-lookup"><span data-stu-id="b8998-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="b8998-121">Section **autres propriétés d'effet**</span><span class="sxs-lookup"><span data-stu-id="b8998-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="b8998-122">Section points de **dégradé de ligne**</span><span class="sxs-lookup"><span data-stu-id="b8998-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="b8998-123">Section points de **dégradé de remplissage**</span><span class="sxs-lookup"><span data-stu-id="b8998-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="b8998-124">Pour obtenir une référence à la cellule **ReplaceLockFormat** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="b8998-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8998-125">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="b8998-125">Cell name:</span></span>  <br/> | <span data-ttu-id="b8998-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="b8998-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="b8998-127">Pour obtenir une référence à la cellule **ReplaceLockFormat** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="b8998-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8998-128">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b8998-128">Section index:</span></span>  <br/> |<span data-ttu-id="b8998-129">**Définis**</span><span class="sxs-lookup"><span data-stu-id="b8998-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b8998-130">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b8998-130">Row index:</span></span>  <br/> |<span data-ttu-id="b8998-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="b8998-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="b8998-132">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b8998-132">Cell index:</span></span>  <br/> |<span data-ttu-id="b8998-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="b8998-133">**visReplaceLockFormat**</span></span> <br/> |
   

