---
title: TypeRotation, cellule (Section Propriétés de Rotation 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Détermine si la forme suit une rotation en parallèle, une rotation du point de vue ou une rotation de l’effet oblique, comme un entier compris entre 0 et 6.
ms.openlocfilehash: 85effcef3969d7b7c57551ec88710ba84b3fc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789532"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="c6a50-103">TypeRotation, cellule (Section Propriétés de Rotation 3D)</span><span class="sxs-lookup"><span data-stu-id="c6a50-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="c6a50-104">Détermine si la forme suit une rotation en parallèle, une rotation du point de vue ou une rotation de l’effet oblique, comme un entier compris entre 0 et 6.</span><span class="sxs-lookup"><span data-stu-id="c6a50-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="c6a50-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c6a50-105">**Value**</span></span>|<span data-ttu-id="c6a50-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="c6a50-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6a50-107">0</span><span class="sxs-lookup"><span data-stu-id="c6a50-107">0</span></span>  <br/> |<span data-ttu-id="c6a50-108">La forme n’a pas de rotation.</span><span class="sxs-lookup"><span data-stu-id="c6a50-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="c6a50-109">1</span><span class="sxs-lookup"><span data-stu-id="c6a50-109">1</span></span>  <br/> |<span data-ttu-id="c6a50-110">La forme est une rotation en parallèle.</span><span class="sxs-lookup"><span data-stu-id="c6a50-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="c6a50-111">2</span><span class="sxs-lookup"><span data-stu-id="c6a50-111">2</span></span>  <br/> |<span data-ttu-id="c6a50-112">La forme est une rotation en perspective.</span><span class="sxs-lookup"><span data-stu-id="c6a50-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="c6a50-113">3</span><span class="sxs-lookup"><span data-stu-id="c6a50-113">3</span></span>  <br/> |<span data-ttu-id="c6a50-114">La forme est une rotation de l’effet oblique supérieure gauche.</span><span class="sxs-lookup"><span data-stu-id="c6a50-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="c6a50-115">4</span><span class="sxs-lookup"><span data-stu-id="c6a50-115">4</span></span>  <br/> |<span data-ttu-id="c6a50-116">La forme est une rotation de l’effet oblique droite supérieure.</span><span class="sxs-lookup"><span data-stu-id="c6a50-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="c6a50-117">5</span><span class="sxs-lookup"><span data-stu-id="c6a50-117">5</span></span>  <br/> |<span data-ttu-id="c6a50-118">La forme est une rotation de l’effet oblique gauche en bas.</span><span class="sxs-lookup"><span data-stu-id="c6a50-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="c6a50-119">6</span><span class="sxs-lookup"><span data-stu-id="c6a50-119">6</span></span>  <br/> |<span data-ttu-id="c6a50-120">La forme possède un bas à droite de rotation de l’effet oblique.</span><span class="sxs-lookup"><span data-stu-id="c6a50-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6a50-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="c6a50-121">Remarks</span></span>

<span data-ttu-id="c6a50-122">Pour obtenir une référence à la cellule **TypeRotation** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c6a50-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6a50-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c6a50-123">Cell name:</span></span>  <br/> |<span data-ttu-id="c6a50-124">TypeRotation</span><span class="sxs-lookup"><span data-stu-id="c6a50-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="c6a50-125">Pour obtenir une référence à la cellule **TypeRotation** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c6a50-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6a50-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c6a50-126">Section index:</span></span>  <br/> |<span data-ttu-id="c6a50-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c6a50-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c6a50-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c6a50-128">Row index:</span></span>  <br/> |<span data-ttu-id="c6a50-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="c6a50-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="c6a50-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c6a50-130">Cell index:</span></span>  <br/> |<span data-ttu-id="c6a50-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="c6a50-131">**visRotationType**</span></span> <br/> |
   

