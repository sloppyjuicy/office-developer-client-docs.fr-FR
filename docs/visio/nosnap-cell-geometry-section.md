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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408543"
---
# <a name="nosnap-cell-geometry-section"></a><span data-ttu-id="be0b7-103">NoSnap, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="be0b7-103">NoSnap Cell (Geometry Section)</span></span>

<span data-ttu-id="be0b7-104">Détermine si les autres formes s'alignent sur un chemin.</span><span class="sxs-lookup"><span data-stu-id="be0b7-104">Determines whether other shapes snap to a path.</span></span>
  
|<span data-ttu-id="be0b7-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="be0b7-105">**Value**</span></span>|<span data-ttu-id="be0b7-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="be0b7-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="be0b7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="be0b7-107">TRUE</span></span>  <br/> | <span data-ttu-id="be0b7-108">Ne permet pas aux autres formes de s'aligner sur ce chemin.</span><span class="sxs-lookup"><span data-stu-id="be0b7-108">Do not allow other shapes to snap to this path.</span></span>  <br/> |
| <span data-ttu-id="be0b7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="be0b7-109">FALSE</span></span>  <br/> | <span data-ttu-id="be0b7-110">Permet aux autres formes de s'aligner sur ce chemin.</span><span class="sxs-lookup"><span data-stu-id="be0b7-110">Allow other shapes to snap to this path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be0b7-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="be0b7-111">Remarks</span></span>

<span data-ttu-id="be0b7-112">Pour obtenir une référence à la cellule NoSnap par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="be0b7-112">To get a reference to the NoSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be0b7-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="be0b7-113">Cell name:</span></span>  <br/> | <span data-ttu-id="be0b7-114">Geometry  *i*  . NoSnap où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="be0b7-114">Geometry  *i*  .NoSnap            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="be0b7-115">Pour obtenir une référence à la cellule NoSnap à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="be0b7-115">To get a reference to the NoSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be0b7-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="be0b7-116">Section index:</span></span>  <br/> |<span data-ttu-id="be0b7-117">**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="be0b7-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="be0b7-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="be0b7-118">Row index:</span></span>  <br/> |<span data-ttu-id="be0b7-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="be0b7-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="be0b7-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="be0b7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="be0b7-121">**visCompNoSnap**</span><span class="sxs-lookup"><span data-stu-id="be0b7-121">**visCompNoSnap**</span></span> <br/> |
   

