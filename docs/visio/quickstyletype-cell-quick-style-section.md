---
title: QuickStyleType Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Détermine le type de style rapide (2 dimensions, 1 dimension ou connecteur) dont hérite la forme.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410503"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="ceaf3-103">QuickStyleType Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="ceaf3-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="ceaf3-104">Détermine le type de style rapide (2 dimensions, 1 dimension ou connecteur) dont hérite la forme.</span><span class="sxs-lookup"><span data-stu-id="ceaf3-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="ceaf3-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ceaf3-105">**Value**</span></span>|<span data-ttu-id="ceaf3-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="ceaf3-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ceaf3-107">0</span><span class="sxs-lookup"><span data-stu-id="ceaf3-107">0</span></span>  <br/> |<span data-ttu-id="ceaf3-108">Visio choisit automatiquement</span><span class="sxs-lookup"><span data-stu-id="ceaf3-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="ceaf3-109">1</span><span class="sxs-lookup"><span data-stu-id="ceaf3-109">1</span></span>  <br/> |<span data-ttu-id="ceaf3-110">1 dimension</span><span class="sxs-lookup"><span data-stu-id="ceaf3-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="ceaf3-111">2</span><span class="sxs-lookup"><span data-stu-id="ceaf3-111">2</span></span>  <br/> |<span data-ttu-id="ceaf3-112">2 dimensions</span><span class="sxs-lookup"><span data-stu-id="ceaf3-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="ceaf3-113">3</span><span class="sxs-lookup"><span data-stu-id="ceaf3-113">3</span></span>  <br/> |<span data-ttu-id="ceaf3-114">Connecteur</span><span class="sxs-lookup"><span data-stu-id="ceaf3-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ceaf3-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="ceaf3-115">Remarks</span></span>

<span data-ttu-id="ceaf3-116">Pour obtenir une référence à la cellule **QuickStyleType** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="ceaf3-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ceaf3-117">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="ceaf3-117">Cell name:</span></span>  <br/> | <span data-ttu-id="ceaf3-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="ceaf3-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="ceaf3-119">Pour obtenir une référence à la **cellule QuickStyleType** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ceaf3-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ceaf3-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ceaf3-120">Section index:</span></span>  <br/> |<span data-ttu-id="ceaf3-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ceaf3-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ceaf3-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ceaf3-122">Row index:</span></span>  <br/> |<span data-ttu-id="ceaf3-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="ceaf3-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="ceaf3-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ceaf3-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ceaf3-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="ceaf3-125">**visQuickStyleType**</span></span> <br/> |
   

