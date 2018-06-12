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
ms.openlocfilehash: 043571243fe3698561bee8632e7fd18db04c9330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789166"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="7ba29-103">NoLiveDynamics, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="7ba29-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="7ba29-104">Détermine si une forme est redimensionnée ou pivote de façon dynamique lorsque vous la manipulez.</span><span class="sxs-lookup"><span data-stu-id="7ba29-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="7ba29-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7ba29-105">**Value**</span></span>|<span data-ttu-id="7ba29-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="7ba29-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7ba29-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7ba29-107">TRUE</span></span>  <br/> | <span data-ttu-id="7ba29-108">La forme n'est pas mise à jour dynamiquement lorsque vous la manipulez.</span><span class="sxs-lookup"><span data-stu-id="7ba29-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="7ba29-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7ba29-109">FALSE</span></span>  <br/> | <span data-ttu-id="7ba29-110">La forme est mise à jour dynamiquement lorsque vous la manipulez.</span><span class="sxs-lookup"><span data-stu-id="7ba29-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ba29-111">Note</span><span class="sxs-lookup"><span data-stu-id="7ba29-111">Remarks</span></span>

<span data-ttu-id="7ba29-p101">Lorsque vous redimensionnez ou faites pivoter une forme 2D sans effets dynamiques, un rectangle de sélection s'affiche. S'il s'agit d'une forme 1D, le retour visuel est basé sur la valeur de la cellule DynFeedback.</span><span class="sxs-lookup"><span data-stu-id="7ba29-p101">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box. If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="7ba29-114">Pour obtenir une référence à la cellule NoLiveDynamics par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="7ba29-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7ba29-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7ba29-115">Cell name:</span></span>  <br/> | <span data-ttu-id="7ba29-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="7ba29-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="7ba29-117">Pour obtenir une référence à la cellule NoLiveDynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7ba29-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7ba29-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7ba29-118">Section index:</span></span>  <br/> |<span data-ttu-id="7ba29-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7ba29-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7ba29-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7ba29-120">Row index:</span></span>  <br/> |<span data-ttu-id="7ba29-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="7ba29-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="7ba29-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7ba29-122">Cell index:</span></span>  <br/> |<span data-ttu-id="7ba29-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="7ba29-123">**visNoLiveDynamics**</span></span> <br/> |
   

