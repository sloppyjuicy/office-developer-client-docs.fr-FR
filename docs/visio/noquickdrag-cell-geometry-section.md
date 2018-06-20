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
description: Détermine si une forme peut être sélectionnée ou déplacée lorsque l’utilisateur clique sur la zone remplie définie par la section Geometry.
ms.openlocfilehash: 7d4ffd876d8676af885b8f750fecf6f6d0deaa9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789178"
---
# <a name="noquickdrag-cell-geometry-section"></a><span data-ttu-id="821e8-103">NoQuickDrag, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="821e8-103">NoQuickDrag Cell (Geometry Section)</span></span>

<span data-ttu-id="821e8-104">Détermine si une forme peut être sélectionnée ou déplacée lorsque l’utilisateur clique sur la zone remplie définie par la section Geometry.</span><span class="sxs-lookup"><span data-stu-id="821e8-104">Determines whether a shape can be selected or dragged when the user clicks the filled area defined by the Geometry section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="821e8-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="821e8-105">Remarks</span></span>

<span data-ttu-id="821e8-106">Pour obtenir une référence à la cellule NoQuickDrag par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="821e8-106">To get a reference to the NoQuickDrag cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="821e8-107">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="821e8-107">Cell name:</span></span>  <br/> |<span data-ttu-id="821e8-108">Géométrie *i* . NoQuickDrag, où * i * - < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="821e8-108">Geometry  *i*  .NoQuickDrag, where  * i *  - <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="821e8-109">Pour obtenir une référence à la cellule NoQuickDrag par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="821e8-109">To get a reference to the NoQuickDrag cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="821e8-110">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="821e8-110">Section index:</span></span>  <br/> |<span data-ttu-id="821e8-111">**visSectionFirstComponent** +  *i* , où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="821e8-111">**visSectionFirstComponent** +  *i*  , where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="821e8-112">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="821e8-112">Row index:</span></span>  <br/> |<span data-ttu-id="821e8-113">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="821e8-113">**visRowComponent**</span></span> <br/> |
|<span data-ttu-id="821e8-114">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="821e8-114">Cell index:</span></span>  <br/> |<span data-ttu-id="821e8-115">**visCompNoQuickDrag**</span><span class="sxs-lookup"><span data-stu-id="821e8-115">**visCompNoQuickDrag**</span></span> <br/> |
   

