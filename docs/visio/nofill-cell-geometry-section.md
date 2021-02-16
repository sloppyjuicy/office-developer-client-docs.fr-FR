---
title: NoFill, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Indique si un chemin peut être rempli.
ms.openlocfilehash: 301f30b644e338ff9e597a7a7d8226b9c8a4462f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415018"
---
# <a name="nofill-cell-geometry-section"></a><span data-ttu-id="198cb-103">NoFill, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="198cb-103">NoFill Cell (Geometry Section)</span></span>

<span data-ttu-id="198cb-104">Indique si un chemin peut être rempli.</span><span class="sxs-lookup"><span data-stu-id="198cb-104">Indicates whether a path can be filled.</span></span>
  
|<span data-ttu-id="198cb-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="198cb-105">**Value**</span></span>|<span data-ttu-id="198cb-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="198cb-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="198cb-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="198cb-107">TRUE</span></span>  <br/> | <span data-ttu-id="198cb-108">Le chemin n'est pas rempli, même si d'autres chemins de la forme sont remplis.</span><span class="sxs-lookup"><span data-stu-id="198cb-108">The path is not filled even if other paths in the shape are filled.</span></span>  <br/> |
| <span data-ttu-id="198cb-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="198cb-109">FALSE</span></span>  <br/> | <span data-ttu-id="198cb-110">Le remplissage de la forme s'applique au chemin, même s'il n'est pas fermé.</span><span class="sxs-lookup"><span data-stu-id="198cb-110">The shape's fill applies to the path, even if it isn't closed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="198cb-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="198cb-111">Remarks</span></span>

<span data-ttu-id="198cb-p101">Si vous définissez le motif de remplissage de la forme sur aucun (0), aucun de ses chemins ne sera rempli. Cette cellule est utilisée pour désactiver de manière sélective le remplissage du chemin d'une forme.</span><span class="sxs-lookup"><span data-stu-id="198cb-p101">If you set a shape's fill pattern to none (0), none of its paths are filled. This cell is used to turn the fill off selectively for a path within a shape.</span></span>
  
<span data-ttu-id="198cb-114">Pour obtenir une référence à la cellule NoFill par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="198cb-114">To get a reference to the NoFill cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="198cb-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="198cb-115">Cell name:</span></span>  <br/> | <span data-ttu-id="198cb-116">Geometry  *i*  . NoFill où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="198cb-116">Geometry  *i*  .NoFill            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="198cb-117">Pour obtenir une référence à la cellule NoFill à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="198cb-117">To get a reference to the NoFill cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="198cb-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="198cb-118">Section index:</span></span>  <br/> |<span data-ttu-id="198cb-119">**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="198cb-119">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="198cb-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="198cb-120">Row index:</span></span>  <br/> |<span data-ttu-id="198cb-121">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="198cb-121">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="198cb-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="198cb-122">Cell index:</span></span>  <br/> |<span data-ttu-id="198cb-123">**visCompNoFill**</span><span class="sxs-lookup"><span data-stu-id="198cb-123">**visCompNoFill**</span></span> <br/> |
   

