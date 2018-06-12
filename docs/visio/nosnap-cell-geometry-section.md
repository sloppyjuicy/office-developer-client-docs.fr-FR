---
title: NoSnap, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Détermine si les autres formes s'alignent sur un chemin.
ms.openlocfilehash: 111f3773cb1df9033ed5a7b0b146d40ce6b26df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789179"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="80e9b-103">NoSnap, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="80e9b-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="80e9b-104">Détermine si les autres formes s'alignent sur un chemin.</span><span class="sxs-lookup"><span data-stu-id="80e9b-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="80e9b-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="80e9b-105">**Value**</span></span>|<span data-ttu-id="80e9b-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="80e9b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="80e9b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="80e9b-107">TRUE</span></span>  <br/> | <span data-ttu-id="80e9b-108">Ne permet pas aux autres formes de s'aligner sur ce chemin.</span><span class="sxs-lookup"><span data-stu-id="80e9b-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="80e9b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="80e9b-109">FALSE</span></span>  <br/> | <span data-ttu-id="80e9b-110">Permet aux autres formes de s'aligner sur ce chemin.</span><span class="sxs-lookup"><span data-stu-id="80e9b-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80e9b-111">Note</span><span class="sxs-lookup"><span data-stu-id="80e9b-111">Remarks</span></span>

<span data-ttu-id="80e9b-112">Pour obtenir une référence à la cellule NoSnap par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="80e9b-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80e9b-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="80e9b-113">Cell name:</span></span>  <br/> | <span data-ttu-id="80e9b-114">Géométrie *i* . NoSnap où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="80e9b-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="80e9b-115">Pour obtenir une référence à la cellule NoSnap par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="80e9b-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80e9b-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="80e9b-116">Section index:</span></span>  <br/> |<span data-ttu-id="80e9b-117">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="80e9b-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="80e9b-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="80e9b-118">Row index:</span></span>  <br/> |<span data-ttu-id="80e9b-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="80e9b-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="80e9b-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="80e9b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="80e9b-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="80e9b-121">**visCompNoSnap**</span></span> <br/> |
   

