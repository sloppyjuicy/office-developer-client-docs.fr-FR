---
title: QuickStyleType Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Détermine le type de style rapide (à deux dimensions, 1D ou connecteur) hérité par la forme.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282578"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="0ce2f-103">QuickStyleType Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="0ce2f-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="0ce2f-104">Détermine le type de style rapide (à deux dimensions, 1D ou connecteur) hérité par la forme.</span><span class="sxs-lookup"><span data-stu-id="0ce2f-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="0ce2f-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="0ce2f-105">**Value**</span></span>|<span data-ttu-id="0ce2f-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="0ce2f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ce2f-107">0</span><span class="sxs-lookup"><span data-stu-id="0ce2f-107">0</span></span>  <br/> |<span data-ttu-id="0ce2f-108">Visio choisit automatiquement</span><span class="sxs-lookup"><span data-stu-id="0ce2f-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="0ce2f-109">0,1</span><span class="sxs-lookup"><span data-stu-id="0ce2f-109">1</span></span>  <br/> |<span data-ttu-id="0ce2f-110">1D</span><span class="sxs-lookup"><span data-stu-id="0ce2f-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="0ce2f-111">n°2</span><span class="sxs-lookup"><span data-stu-id="0ce2f-111">2</span></span>  <br/> |<span data-ttu-id="0ce2f-112">2D</span><span class="sxs-lookup"><span data-stu-id="0ce2f-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="0ce2f-113">3</span><span class="sxs-lookup"><span data-stu-id="0ce2f-113">3</span></span>  <br/> |<span data-ttu-id="0ce2f-114">Connector</span><span class="sxs-lookup"><span data-stu-id="0ce2f-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ce2f-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="0ce2f-115">Remarks</span></span>

<span data-ttu-id="0ce2f-116">Pour obtenir une référence à la cellule **QuickStyleType** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="0ce2f-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ce2f-117">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="0ce2f-117">Cell name:</span></span>  <br/> | <span data-ttu-id="0ce2f-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="0ce2f-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="0ce2f-119">Pour obtenir une référence à la cellule **QuickStyleType** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="0ce2f-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ce2f-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="0ce2f-120">Section index:</span></span>  <br/> |<span data-ttu-id="0ce2f-121">**Définis**</span><span class="sxs-lookup"><span data-stu-id="0ce2f-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0ce2f-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="0ce2f-122">Row index:</span></span>  <br/> |<span data-ttu-id="0ce2f-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="0ce2f-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="0ce2f-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0ce2f-124">Cell index:</span></span>  <br/> |<span data-ttu-id="0ce2f-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="0ce2f-125">**visQuickStyleType**</span></span> <br/> |
   

