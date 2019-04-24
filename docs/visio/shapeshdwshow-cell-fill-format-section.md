---
title: ShapeShdwShow Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Détermine si la forme affiche une ombre, sous la forme d'un nombre entier compris entre 0 et 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349146"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="11fd5-103">ShapeShdwShow Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="11fd5-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="11fd5-104">Détermine si la forme affiche une ombre, sous la forme d'un nombre entier compris entre 0 et 2.</span><span class="sxs-lookup"><span data-stu-id="11fd5-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="11fd5-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="11fd5-105">**Value**</span></span>|<span data-ttu-id="11fd5-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="11fd5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="11fd5-107">0</span><span class="sxs-lookup"><span data-stu-id="11fd5-107">0</span></span>  <br/> |<span data-ttu-id="11fd5-108">Affiche toujours l'ombre si une ombre est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="11fd5-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="11fd5-109">Les ombres des sous-formes ne sont pas affichées.</span><span class="sxs-lookup"><span data-stu-id="11fd5-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="11fd5-110">0,1</span><span class="sxs-lookup"><span data-stu-id="11fd5-110">1</span></span>  <br/> |<span data-ttu-id="11fd5-111">Ne pas afficher d'ombre, sauf si la forme n'a pas de parent.</span><span class="sxs-lookup"><span data-stu-id="11fd5-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="11fd5-112">Utiliser des ombres de sous-formes si elles sont regroupées.</span><span class="sxs-lookup"><span data-stu-id="11fd5-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="11fd5-113">n°2</span><span class="sxs-lookup"><span data-stu-id="11fd5-113">2</span></span>  <br/> |<span data-ttu-id="11fd5-114">Affiche toujours une ombre si une ombre est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="11fd5-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="11fd5-115">Les ombres des sous-formes sont affichées.</span><span class="sxs-lookup"><span data-stu-id="11fd5-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11fd5-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="11fd5-116">Remarks</span></span>

<span data-ttu-id="11fd5-117">Pour obtenir une référence à la cellule **ShapeShdwShow** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="11fd5-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11fd5-118">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="11fd5-118">Cell name:</span></span>  <br/> | <span data-ttu-id="11fd5-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="11fd5-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="11fd5-120">Pour obtenir une référence à la cellule **ShapeShdwShow** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="11fd5-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11fd5-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="11fd5-121">Section index:</span></span>  <br/> |<span data-ttu-id="11fd5-122">**Définis**</span><span class="sxs-lookup"><span data-stu-id="11fd5-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="11fd5-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="11fd5-123">Row index:</span></span>  <br/> |<span data-ttu-id="11fd5-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="11fd5-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="11fd5-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="11fd5-125">Cell index:</span></span>  <br/> |<span data-ttu-id="11fd5-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="11fd5-126">**visFillShdwShow**</span></span> <br/> |
   

