---
title: Cellule Angle (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: "Représente l'angle de rotation actuel de la forme par rapport à son parent. La formule par défaut déterminant l'angle de rotation d'une forme 1D est : =ATAN2(EndY-BeginY,EndX-BeginX)."
ms.openlocfilehash: 85f64c6111b492940d278a5558508a2dea6b1e1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414549"
---
# <a name="angle-cell-shape-transform-section"></a><span data-ttu-id="b7129-104">Cellule Angle (section Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="b7129-104">Angle Cell (Shape Transform Section)</span></span>

<span data-ttu-id="b7129-p102">Représente l'angle de rotation actuel de la forme par rapport à son parent. La formule par défaut déterminant l'angle de rotation d'une forme 1D est : =ATAN2(EndY-BeginY,EndX-BeginX).</span><span class="sxs-lookup"><span data-stu-id="b7129-p102">Represents the shape's current angle of rotation in relation to its parent. The default formula for determining the rotation angle of a 1-D shape is: =ATAN2(EndY-BeginY,EndX-BeginX).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7129-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="b7129-107">Remarks</span></span>

<span data-ttu-id="b7129-108">Pour obtenir une référence à la cellule Angle par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b7129-108">To get a reference to the Angle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7129-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b7129-109">Cell name:</span></span>  <br/> | <span data-ttu-id="b7129-110">Angle</span><span class="sxs-lookup"><span data-stu-id="b7129-110">Angle</span></span>  <br/> |
   
<span data-ttu-id="b7129-111">Pour obtenir une référence à la cellule Angle à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b7129-111">To get a reference to the Angle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7129-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b7129-112">Section index:</span></span>  <br/> |<span data-ttu-id="b7129-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b7129-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b7129-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b7129-114">Row index:</span></span>  <br/> |<span data-ttu-id="b7129-115">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="b7129-115">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="b7129-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b7129-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b7129-117">**visXFormAngle**</span><span class="sxs-lookup"><span data-stu-id="b7129-117">**visXFormAngle**</span></span> <br/> |
   

