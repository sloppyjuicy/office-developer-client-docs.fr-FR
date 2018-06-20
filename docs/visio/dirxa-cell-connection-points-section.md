---
title: DirX / A, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Détermine le x-composant requis vecteur d’alignement d’un point de connexion correspondant. Le DirX / une cellule est également utilisée pour orienter la branche reliée d’un connecteur dynamique. Cette cellule prend flottante valeur du point.
ms.openlocfilehash: 49feba7cefbccc4efcbd04e8940c1f801563539e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788492"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="d44a8-105">DirX / A, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="d44a8-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="d44a8-106">Détermine le *x* -composant requis vecteur d’alignement d’un point de connexion correspondant.</span><span class="sxs-lookup"><span data-stu-id="d44a8-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="d44a8-107">Le DirX / une cellule est également utilisée pour orienter la branche reliée d’un connecteur dynamique.</span><span class="sxs-lookup"><span data-stu-id="d44a8-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="d44a8-108">Cette cellule prend flottante valeur du point.</span><span class="sxs-lookup"><span data-stu-id="d44a8-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d44a8-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="d44a8-109">Remarks</span></span>

<span data-ttu-id="d44a8-110">Pour obtenir une référence à la DirX / une cellule par un nom à partir d’une autre formule ou d’un programme à l’aide de la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="d44a8-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d44a8-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d44a8-111">Cell name:</span></span>  <br/> | <span data-ttu-id="d44a8-112">Connections.DirX [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d44a8-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d44a8-113">Pour obtenir une référence à la DirX / une cellule par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d44a8-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d44a8-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d44a8-114">Section index:</span></span>  <br/> |<span data-ttu-id="d44a8-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="d44a8-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="d44a8-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d44a8-116">Row index:</span></span>  <br/> |<span data-ttu-id="d44a8-117">**visRowConnectionPts** +  *i* où *i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="d44a8-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="d44a8-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d44a8-118">Cell index:</span></span>  <br/> |<span data-ttu-id="d44a8-119">**visCnnctDirX** (lignes non étendues)           **visCnnctA** (lignes étendues)</span><span class="sxs-lookup"><span data-stu-id="d44a8-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="d44a8-120">Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.</span><span class="sxs-lookup"><span data-stu-id="d44a8-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

