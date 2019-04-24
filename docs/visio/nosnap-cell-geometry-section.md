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
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341129"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="67649-103">NoSnap, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="67649-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="67649-104">Détermine si les autres formes s'alignent sur un chemin.</span><span class="sxs-lookup"><span data-stu-id="67649-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="67649-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="67649-105">**Value**</span></span>|<span data-ttu-id="67649-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="67649-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="67649-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="67649-107">TRUE</span></span>  <br/> | <span data-ttu-id="67649-108">Ne permet pas aux autres formes de s'aligner sur ce chemin.</span><span class="sxs-lookup"><span data-stu-id="67649-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="67649-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="67649-109">FALSE</span></span>  <br/> | <span data-ttu-id="67649-110">Permet aux autres formes de s'aligner sur ce chemin.</span><span class="sxs-lookup"><span data-stu-id="67649-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67649-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="67649-111">Remarks</span></span>

<span data-ttu-id="67649-112">Pour obtenir une référence à la cellule NoSnap par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="67649-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67649-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="67649-113">Cell name:</span></span>  <br/> | <span data-ttu-id="67649-114">Géométrie *i* . NoSnap où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="67649-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="67649-115">Pour obtenir une référence à la cellule NoSnap à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="67649-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67649-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="67649-116">Section index:</span></span>  <br/> |<span data-ttu-id="67649-117">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="67649-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="67649-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="67649-118">Row index:</span></span>  <br/> |<span data-ttu-id="67649-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="67649-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="67649-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="67649-120">Cell index:</span></span>  <br/> |<span data-ttu-id="67649-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="67649-121">**visCompNoSnap**</span></span> <br/> |
   

