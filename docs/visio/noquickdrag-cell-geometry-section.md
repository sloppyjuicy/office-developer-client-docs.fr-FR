---
title: NoQuickDrag, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Détermine si une forme peut être sélectionnée ou déplacée lorsque l'utilisateur clique sur la zone remplie définie par la section Geometry.
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417720"
---
# <a name="noquickdrag-cell-geometry-section"></a><span data-ttu-id="639e0-103">NoQuickDrag, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="639e0-103">NoQuickDrag Cell (Geometry Section)</span></span>

<span data-ttu-id="639e0-104">Détermine si une forme peut être sélectionnée ou déplacée lorsque l'utilisateur clique sur la zone remplie définie par la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="639e0-104">Determines whether a shape can be selected or dragged when the user clicks the filled area defined by the Geometry section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="639e0-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="639e0-105">Remarks</span></span>

<span data-ttu-id="639e0-106">Pour obtenir une référence à la cellule NoQuickDrag par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="639e0-106">To get a reference to the NoQuickDrag cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="639e0-107">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="639e0-107">Cell name:</span></span>  <br/> |<span data-ttu-id="639e0-108">Géométrie *i* . NoQuickDrag, où \* i \*-<1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="639e0-108">Geometry  *i*  .NoQuickDrag, where  \* i \*  - <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="639e0-109">Pour obtenir une référence à la cellule NoQuickDrag à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="639e0-109">To get a reference to the NoQuickDrag cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="639e0-110">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="639e0-110">Section index:</span></span>  <br/> |<span data-ttu-id="639e0-111">**visSectionFirstComponent** +  *i* , où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="639e0-111">**visSectionFirstComponent** +  *i*  , where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="639e0-112">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="639e0-112">Row index:</span></span>  <br/> |<span data-ttu-id="639e0-113">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="639e0-113">**visRowComponent**</span></span> <br/> |
|<span data-ttu-id="639e0-114">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="639e0-114">Cell index:</span></span>  <br/> |<span data-ttu-id="639e0-115">**visCompNoQuickDrag**</span><span class="sxs-lookup"><span data-stu-id="639e0-115">**visCompNoQuickDrag**</span></span> <br/> |
   

