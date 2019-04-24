---
title: D, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Cellule de montage utilisable pour entrer ou tester des formules.
ms.openlocfilehash: e7bd61b8bc7a1a3b765af738681d958e2c83ba05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345086"
---
# <a name="d-cell-connection-points-section"></a><span data-ttu-id="9dcdd-103">D, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="9dcdd-103">D Cell (Connection Points Section)</span></span>

<span data-ttu-id="9dcdd-104">Cellule de montage utilisable pour entrer ou tester des formules.</span><span class="sxs-lookup"><span data-stu-id="9dcdd-104">A scratch cell that you can use for entering or testing formulas.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9dcdd-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="9dcdd-105">Remarks</span></span>

<span data-ttu-id="9dcdd-106">Pour accéder à la cellule D, cliquez avec le bouton droit de la souris sur une ligne, puis cliquez sur **Modifier le type de ligne** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="9dcdd-106">To access the D cell, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  
<span data-ttu-id="9dcdd-107">Pour obtenir une référence à la cellule D par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9dcdd-107">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9dcdd-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9dcdd-108">Cell name:</span></span>  <br/> | <span data-ttu-id="9dcdd-109">Connections. D [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9dcdd-109">Connections.D[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9dcdd-110">Pour obtenir une référence à la cellule D à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9dcdd-110">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9dcdd-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9dcdd-111">Section index:</span></span>  <br/> |<span data-ttu-id="9dcdd-112">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="9dcdd-112">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="9dcdd-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9dcdd-113">Row index:</span></span>  <br/> |<span data-ttu-id="9dcdd-114">**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9dcdd-114">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9dcdd-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9dcdd-115">Cell index:</span></span>  <br/> |<span data-ttu-id="9dcdd-116">**visCnnctD**</span><span class="sxs-lookup"><span data-stu-id="9dcdd-116">**visCnnctD**</span></span> <br/> |
   

