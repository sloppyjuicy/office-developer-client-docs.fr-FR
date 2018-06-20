---
title: ShapeShdwShow, cellule (Section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Détermine si la forme affiche une ombre, comme un entier compris entre 0 et 2.
ms.openlocfilehash: 72077e60089acd3cd3f8a9349691e1468f6b1f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789667"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="16aaa-103">ShapeShdwShow, cellule (Section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="16aaa-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="16aaa-104">Détermine si la forme affiche une ombre, comme un entier compris entre 0 et 2.</span><span class="sxs-lookup"><span data-stu-id="16aaa-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="16aaa-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="16aaa-105">**Value**</span></span>|<span data-ttu-id="16aaa-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="16aaa-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="16aaa-107">0</span><span class="sxs-lookup"><span data-stu-id="16aaa-107">0</span></span>  <br/> |<span data-ttu-id="16aaa-108">Toujours afficher l’ombre si une ombre est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="16aaa-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="16aaa-109">Les ombres pour sous-formes ne sont pas affichées.</span><span class="sxs-lookup"><span data-stu-id="16aaa-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="16aaa-110">1</span><span class="sxs-lookup"><span data-stu-id="16aaa-110">1</span></span>  <br/> |<span data-ttu-id="16aaa-111">Ne s’affichent pas une ombre, sauf si la forme n’a pas de parent.</span><span class="sxs-lookup"><span data-stu-id="16aaa-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="16aaa-112">Utilisez les ombres sous forme si regroupés.</span><span class="sxs-lookup"><span data-stu-id="16aaa-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="16aaa-113">2</span><span class="sxs-lookup"><span data-stu-id="16aaa-113">2</span></span>  <br/> |<span data-ttu-id="16aaa-114">Toujours afficher une ombre si une ombre est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="16aaa-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="16aaa-115">Les ombres pour les formes secondaires sont affichées.</span><span class="sxs-lookup"><span data-stu-id="16aaa-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16aaa-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="16aaa-116">Remarks</span></span>

<span data-ttu-id="16aaa-117">Pour obtenir une référence à la cellule **ShapeShdwShow** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="16aaa-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16aaa-118">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="16aaa-118">Cell name:</span></span>  <br/> | <span data-ttu-id="16aaa-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="16aaa-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="16aaa-120">Pour obtenir une référence à la cellule **ShapeShdwShow** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="16aaa-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16aaa-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="16aaa-121">Section index:</span></span>  <br/> |<span data-ttu-id="16aaa-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="16aaa-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="16aaa-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="16aaa-123">Row index:</span></span>  <br/> |<span data-ttu-id="16aaa-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="16aaa-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="16aaa-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="16aaa-125">Cell index:</span></span>  <br/> |<span data-ttu-id="16aaa-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="16aaa-126">**visFillShdwShow**</span></span> <br/> |
   

