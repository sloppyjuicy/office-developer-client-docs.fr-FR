---
title: NoLiveDynamics, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Détermine si une forme est redimensionnée ou pivote de façon dynamique lorsque vous la manipulez.
ms.openlocfilehash: e332546c1fc5dfc71dfa3b72ea5a58bfef59dc7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421479"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="5c780-103">NoLiveDynamics, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="5c780-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="5c780-104">Détermine si une forme est redimensionnée ou pivote de façon dynamique lorsque vous la manipulez.</span><span class="sxs-lookup"><span data-stu-id="5c780-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="5c780-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5c780-105">**Value**</span></span>|<span data-ttu-id="5c780-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="5c780-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5c780-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5c780-107">TRUE</span></span>  <br/> | <span data-ttu-id="5c780-108">La forme n'est pas mise à jour dynamiquement lorsque vous la manipulez.</span><span class="sxs-lookup"><span data-stu-id="5c780-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="5c780-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5c780-109">FALSE</span></span>  <br/> | <span data-ttu-id="5c780-110">La forme est mise à jour dynamiquement lorsque vous la manipulez.</span><span class="sxs-lookup"><span data-stu-id="5c780-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c780-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c780-111">Remarks</span></span>

<span data-ttu-id="5c780-p101">Lorsque vous redimensionnez ou faites pivoter une forme 2D sans effets dynamiques, un rectangle de sélection s'affiche. S'il s'agit d'une forme 1D, le retour visuel est basé sur la valeur de la cellule DynFeedback.</span><span class="sxs-lookup"><span data-stu-id="5c780-p101">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box. If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="5c780-114">Pour obtenir une référence à la cellule NoLiveDynamics par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="5c780-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c780-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5c780-115">Cell name:</span></span>  <br/> | <span data-ttu-id="5c780-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="5c780-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="5c780-117">Pour obtenir une référence à la cellule NoLiveDynamics à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5c780-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c780-118">Index de la section  :</span><span class="sxs-lookup"><span data-stu-id="5c780-118">Section index:</span></span>  <br/> |<span data-ttu-id="5c780-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5c780-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5c780-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5c780-120">Row index:</span></span>  <br/> |<span data-ttu-id="5c780-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="5c780-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="5c780-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5c780-122">Cell index:</span></span>  <br/> |<span data-ttu-id="5c780-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="5c780-123">**visNoLiveDynamics**</span></span> <br/> |
   

