---
title: E, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Contient une formule de courbe B-spline rationnelle non uniforme (NURBS).
ms.openlocfilehash: 000c4864c6ae98bfcd9e9cfdb16ff68396f63e44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788541"
---
# <a name="e-cell-geometry-section"></a><span data-ttu-id="16f9c-103">E, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="16f9c-103">E Cell (Geometry Section)</span></span>

<span data-ttu-id="16f9c-104">Contient une formule de courbe B-spline rationnelle non uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="16f9c-104">Contains a nonuniform rational B-spline (NURBS) formula.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16f9c-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="16f9c-105">Remarks</span></span>

<span data-ttu-id="16f9c-106">Pour obtenir une référence à la cellule E par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="16f9c-106">To get a reference to the E cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16f9c-107">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="16f9c-107">Cell name:</span></span>  <br/> | <span data-ttu-id="16f9c-108">Géométrie *i* . E *j* où *i* et *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="16f9c-108">Geometry  *i*  .E  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="16f9c-109">Pour obtenir une référence à la cellule E par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="16f9c-109">To get a reference to the E cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16f9c-110">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="16f9c-110">Section index:</span></span>  <br/> |<span data-ttu-id="16f9c-111">**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="16f9c-111">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="16f9c-112">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="16f9c-112">Row index:</span></span>  <br/> |<span data-ttu-id="16f9c-113">**visRowVertex** +  *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="16f9c-113">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="16f9c-114">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="16f9c-114">Cell index:</span></span>  <br/> |<span data-ttu-id="16f9c-115">**visNURBSData**</span><span class="sxs-lookup"><span data-stu-id="16f9c-115">**visNURBSData**</span></span> <br/> |
   

