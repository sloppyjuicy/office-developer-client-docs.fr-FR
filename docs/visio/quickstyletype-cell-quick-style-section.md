---
title: QuickStyleType, cellule (Section Style rapide)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Détermine le type de Style rapide (2D, 1D, ou le connecteur) qui hérite de la forme.
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789383"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="2cd21-103">QuickStyleType, cellule (Section Style rapide)</span><span class="sxs-lookup"><span data-stu-id="2cd21-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="2cd21-104">Détermine le type de Style rapide (2D, 1D, ou le connecteur) qui hérite de la forme.</span><span class="sxs-lookup"><span data-stu-id="2cd21-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="2cd21-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2cd21-105">**Value**</span></span>|<span data-ttu-id="2cd21-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="2cd21-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2cd21-107">0</span><span class="sxs-lookup"><span data-stu-id="2cd21-107">0</span></span>  <br/> |<span data-ttu-id="2cd21-108">Visio choisit automatiquement</span><span class="sxs-lookup"><span data-stu-id="2cd21-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="2cd21-109">1</span><span class="sxs-lookup"><span data-stu-id="2cd21-109">1</span></span>  <br/> |<span data-ttu-id="2cd21-110">1D</span><span class="sxs-lookup"><span data-stu-id="2cd21-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="2cd21-111">2</span><span class="sxs-lookup"><span data-stu-id="2cd21-111">2</span></span>  <br/> |<span data-ttu-id="2cd21-112">2D</span><span class="sxs-lookup"><span data-stu-id="2cd21-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="2cd21-113">3</span><span class="sxs-lookup"><span data-stu-id="2cd21-113">3</span></span>  <br/> |<span data-ttu-id="2cd21-114">Connecteur</span><span class="sxs-lookup"><span data-stu-id="2cd21-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cd21-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="2cd21-115">Remarks</span></span>

<span data-ttu-id="2cd21-116">Pour obtenir une référence à la cellule **QuickStyleType** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="2cd21-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2cd21-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2cd21-117">Cell name:</span></span>  <br/> | <span data-ttu-id="2cd21-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="2cd21-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="2cd21-119">Pour obtenir une référence à la cellule **QuickStyleType** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2cd21-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2cd21-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2cd21-120">Section index:</span></span>  <br/> |<span data-ttu-id="2cd21-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2cd21-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2cd21-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2cd21-122">Row index:</span></span>  <br/> |<span data-ttu-id="2cd21-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="2cd21-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="2cd21-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2cd21-124">Cell index:</span></span>  <br/> |<span data-ttu-id="2cd21-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="2cd21-125">**visQuickStyleType**</span></span> <br/> |
   

