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
description: Détermine le composant x pour le vecteur d’alignement requis d’un point de connexion correspondant. La cellule DirX / A sert également à orienter la branche reliée d'un connecteur dynamique. Cette cellule prend pour valeur un réel à virgule flottante.
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422396"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="e8a07-105">DirX / A, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="e8a07-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="e8a07-106">Détermine le  *composant x pour*  le vecteur d’alignement requis d’un point de connexion correspondant.</span><span class="sxs-lookup"><span data-stu-id="e8a07-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="e8a07-107">La cellule DirX / A sert également à orienter la branche reliée d'un connecteur dynamique.</span><span class="sxs-lookup"><span data-stu-id="e8a07-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="e8a07-108">Cette cellule prend pour valeur un réel à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="e8a07-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e8a07-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8a07-109">Remarks</span></span>

<span data-ttu-id="e8a07-110">Pour obtenir une référence à la cellule DirX / A par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="e8a07-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8a07-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e8a07-111">Cell name:</span></span>  <br/> | <span data-ttu-id="e8a07-112">Connections.DirX[  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e8a07-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e8a07-113">Pour obtenir une référence à la cellule DirX / A à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e8a07-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8a07-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e8a07-114">Section index:</span></span>  <br/> |<span data-ttu-id="e8a07-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="e8a07-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="e8a07-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e8a07-116">Row index:</span></span>  <br/> |<span data-ttu-id="e8a07-117">**visRowConnectionPts**  +   *i* où *i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="e8a07-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="e8a07-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e8a07-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e8a07-119">**visCnnctDirX** (lignes non étendues)           **visCnnctA** (lignes étendues)</span><span class="sxs-lookup"><span data-stu-id="e8a07-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="e8a07-120">Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.</span><span class="sxs-lookup"><span data-stu-id="e8a07-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

