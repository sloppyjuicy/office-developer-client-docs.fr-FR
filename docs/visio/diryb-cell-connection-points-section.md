---
title: DirY / B, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Détermine la valeur y-composant requis vecteur d’alignement d’un point de connexion correspondant. Il est également utilisé pour orienter la branche reliée d’un connecteur dynamique. Cette cellule prend flottante valeur du point.
ms.openlocfilehash: e650e598b1e47d666b2700d683a17300d3a8e67d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788463"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="05e5d-105">DirY / B, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="05e5d-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="05e5d-106">Détermine la valeur *y* -composant requis vecteur d’alignement d’un point de connexion correspondant.</span><span class="sxs-lookup"><span data-stu-id="05e5d-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="05e5d-107">Il est également utilisé pour orienter la branche reliée d’un connecteur dynamique.</span><span class="sxs-lookup"><span data-stu-id="05e5d-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="05e5d-108">Cette cellule prend flottante valeur du point.</span><span class="sxs-lookup"><span data-stu-id="05e5d-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="05e5d-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="05e5d-109">Remarks</span></span>

<span data-ttu-id="05e5d-110">Pour obtenir une référence à la DirY / B, cellule par un nom à partir d’une autre formule ou d’un programme à l’aide de la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="05e5d-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05e5d-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="05e5d-111">Cell name:</span></span>  <br/> |<span data-ttu-id="05e5d-112">Connections.DirY [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="05e5d-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="05e5d-113">Pour obtenir une référence à la DirY / B, cellule par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="05e5d-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05e5d-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="05e5d-114">Section index:</span></span>  <br/> |<span data-ttu-id="05e5d-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="05e5d-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="05e5d-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="05e5d-116">Row index:</span></span>  <br/> |<span data-ttu-id="05e5d-117">**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="05e5d-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="05e5d-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="05e5d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="05e5d-119">**visCnnctDirY** (lignes non étendues)           **visCnnctB** (lignes étendues)</span><span class="sxs-lookup"><span data-stu-id="05e5d-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="05e5d-120">Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.</span><span class="sxs-lookup"><span data-stu-id="05e5d-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

