---
title: RotationType Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Détermine si la forme suit une rotation parallèle, une rotation de perspective ou une rotation oblique, sous la forme d’un nombre integer de 0 à 6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422942"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="84ca1-103">RotationType Cell (3-D Rotation Properties Section)</span><span class="sxs-lookup"><span data-stu-id="84ca1-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="84ca1-104">Détermine si la forme suit une rotation parallèle, une rotation de perspective ou une rotation oblique, sous la forme d’un nombre integer de 0 à 6.</span><span class="sxs-lookup"><span data-stu-id="84ca1-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="84ca1-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="84ca1-105">**Value**</span></span>|<span data-ttu-id="84ca1-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="84ca1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="84ca1-107">0</span><span class="sxs-lookup"><span data-stu-id="84ca1-107">0</span></span>  <br/> |<span data-ttu-id="84ca1-108">La forme n’a aucune rotation.</span><span class="sxs-lookup"><span data-stu-id="84ca1-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="84ca1-109">1 </span><span class="sxs-lookup"><span data-stu-id="84ca1-109">1</span></span>  <br/> |<span data-ttu-id="84ca1-110">La forme a une rotation parallèle.</span><span class="sxs-lookup"><span data-stu-id="84ca1-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="84ca1-111">2 </span><span class="sxs-lookup"><span data-stu-id="84ca1-111">2</span></span>  <br/> |<span data-ttu-id="84ca1-112">La forme a une rotation de perspective.</span><span class="sxs-lookup"><span data-stu-id="84ca1-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="84ca1-113">3 </span><span class="sxs-lookup"><span data-stu-id="84ca1-113">3</span></span>  <br/> |<span data-ttu-id="84ca1-114">La forme possède une rotation oblique supérieure gauche.</span><span class="sxs-lookup"><span data-stu-id="84ca1-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="84ca1-115">4 </span><span class="sxs-lookup"><span data-stu-id="84ca1-115">4</span></span>  <br/> |<span data-ttu-id="84ca1-116">La forme possède une rotation oblique supérieure droite.</span><span class="sxs-lookup"><span data-stu-id="84ca1-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="84ca1-117">5 </span><span class="sxs-lookup"><span data-stu-id="84ca1-117">5</span></span>  <br/> |<span data-ttu-id="84ca1-118">La forme a une rotation oblique vers le bas à gauche.</span><span class="sxs-lookup"><span data-stu-id="84ca1-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="84ca1-119">6 </span><span class="sxs-lookup"><span data-stu-id="84ca1-119">6</span></span>  <br/> |<span data-ttu-id="84ca1-120">La forme a une rotation oblique vers le bas à droite.</span><span class="sxs-lookup"><span data-stu-id="84ca1-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84ca1-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="84ca1-121">Remarks</span></span>

<span data-ttu-id="84ca1-122">Pour obtenir une référence à la cellule **RotationType** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="84ca1-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84ca1-123">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="84ca1-123">Cell name:</span></span>  <br/> |<span data-ttu-id="84ca1-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="84ca1-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="84ca1-125">Pour obtenir une référence à la cellule **RotationType** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="84ca1-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84ca1-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="84ca1-126">Section index:</span></span>  <br/> |<span data-ttu-id="84ca1-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="84ca1-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="84ca1-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="84ca1-128">Row index:</span></span>  <br/> |<span data-ttu-id="84ca1-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="84ca1-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="84ca1-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="84ca1-130">Cell index:</span></span>  <br/> |<span data-ttu-id="84ca1-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="84ca1-131">**visRotationType**</span></span> <br/> |
   

