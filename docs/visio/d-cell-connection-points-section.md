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
ms.openlocfilehash: 21c81c7a0a64c3016d8cff3b33d83ce785dc24eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788396"
---
# <a name="d-cell-connection-points-section"></a><span data-ttu-id="fa3c8-103">D, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="fa3c8-103">D Cell (Connection Points Section)</span></span>

<span data-ttu-id="fa3c8-104">Cellule de montage utilisable pour entrer ou tester des formules.</span><span class="sxs-lookup"><span data-stu-id="fa3c8-104">A scratch cell that you can use for entering or testing formulas.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa3c8-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa3c8-105">Remarks</span></span>

<span data-ttu-id="fa3c8-106">Pour accéder à la cellule D, cliquez sur une ligne, puis cliquez sur **Modifier le Type de ligne** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fa3c8-106">To access the D cell, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  
<span data-ttu-id="fa3c8-107">Pour obtenir une référence à la cellule D par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="fa3c8-107">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa3c8-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fa3c8-108">Cell name:</span></span>  <br/> | <span data-ttu-id="fa3c8-109">Connections.D [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fa3c8-109">Connections.D[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fa3c8-110">Pour obtenir une référence à la cellule D par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="fa3c8-110">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa3c8-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fa3c8-111">Section index:</span></span>  <br/> |<span data-ttu-id="fa3c8-112">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="fa3c8-112">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="fa3c8-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fa3c8-113">Row index:</span></span>  <br/> |<span data-ttu-id="fa3c8-114">**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fa3c8-114">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fa3c8-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fa3c8-115">Cell index:</span></span>  <br/> |<span data-ttu-id="fa3c8-116">**visCnnctD**</span><span class="sxs-lookup"><span data-stu-id="fa3c8-116">**visCnnctD**</span></span> <br/> |
   

