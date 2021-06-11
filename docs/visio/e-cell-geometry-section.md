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
ms.openlocfilehash: 5c9b3cbf96e2a218a8ed790d3a5615843360c95e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423565"
---
# <a name="e-cell-geometry-section"></a><span data-ttu-id="54c63-103">E, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="54c63-103">E Cell (Geometry Section)</span></span>

<span data-ttu-id="54c63-104">Contient une formule de courbe B-spline rationnelle non uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="54c63-104">Contains a nonuniform rational B-spline (NURBS) formula.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54c63-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="54c63-105">Remarks</span></span>

<span data-ttu-id="54c63-106">Pour obtenir une référence à la cellule E par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="54c63-106">To get a reference to the E cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54c63-107">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="54c63-107">Cell name:</span></span>  <br/> | <span data-ttu-id="54c63-108">Geometry  *i*  . E  *j*            où  *i et*  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="54c63-108">Geometry  *i*  .E  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="54c63-109">Pour obtenir une référence à la cellule E à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="54c63-109">To get a reference to the E cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54c63-110">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="54c63-110">Section index:</span></span>  <br/> |<span data-ttu-id="54c63-111">**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="54c63-111">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="54c63-112">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="54c63-112">Row index:</span></span>  <br/> |<span data-ttu-id="54c63-113">**visRowVertex**  +   *j* où *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="54c63-113">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="54c63-114">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="54c63-114">Cell index:</span></span>  <br/> |<span data-ttu-id="54c63-115">**visNURBSData**</span><span class="sxs-lookup"><span data-stu-id="54c63-115">**visNURBSData**</span></span> <br/> |
   

