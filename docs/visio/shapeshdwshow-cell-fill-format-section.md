---
title: ShapeShdwShow Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Détermine si la forme affiche une ombre, sous la forme d’un nombre integer de 0 à 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422116"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="d5cb8-103">ShapeShdwShow Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="d5cb8-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="d5cb8-104">Détermine si la forme affiche une ombre, sous la forme d’un nombre integer de 0 à 2.</span><span class="sxs-lookup"><span data-stu-id="d5cb8-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="d5cb8-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="d5cb8-105">**Value**</span></span>|<span data-ttu-id="d5cb8-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="d5cb8-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5cb8-107">0</span><span class="sxs-lookup"><span data-stu-id="d5cb8-107">0</span></span>  <br/> |<span data-ttu-id="d5cb8-108">Toujours afficher l’ombre si une ombre est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d5cb8-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="d5cb8-109">Les ombres des sous-formes ne sont pas affichées.</span><span class="sxs-lookup"><span data-stu-id="d5cb8-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="d5cb8-110">1 </span><span class="sxs-lookup"><span data-stu-id="d5cb8-110">1</span></span>  <br/> |<span data-ttu-id="d5cb8-111">Ne restituer une ombre que si la forme n’a pas de parent.</span><span class="sxs-lookup"><span data-stu-id="d5cb8-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="d5cb8-112">Utilisez des ombres de sous-forme si elles sont regroupées.</span><span class="sxs-lookup"><span data-stu-id="d5cb8-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="d5cb8-113">2 </span><span class="sxs-lookup"><span data-stu-id="d5cb8-113">2</span></span>  <br/> |<span data-ttu-id="d5cb8-114">Toujours afficher une ombre si une ombre est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d5cb8-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="d5cb8-115">Les ombres des sous-formes sont affichées.</span><span class="sxs-lookup"><span data-stu-id="d5cb8-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5cb8-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d5cb8-116">Remarks</span></span>

<span data-ttu-id="d5cb8-117">Pour obtenir une référence à la cellule **ShapeShdwShow** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="d5cb8-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d5cb8-118">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="d5cb8-118">Cell name:</span></span>  <br/> | <span data-ttu-id="d5cb8-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="d5cb8-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="d5cb8-120">Pour obtenir une référence à la **cellule ShapeShdwShow** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d5cb8-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d5cb8-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d5cb8-121">Section index:</span></span>  <br/> |<span data-ttu-id="d5cb8-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d5cb8-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d5cb8-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d5cb8-123">Row index:</span></span>  <br/> |<span data-ttu-id="d5cb8-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="d5cb8-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="d5cb8-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d5cb8-125">Cell index:</span></span>  <br/> |<span data-ttu-id="d5cb8-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="d5cb8-126">**visFillShdwShow**</span></span> <br/> |
   

