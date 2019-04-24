---
title: DropOnPageScale, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: 17c597df3d9e7e741d902fd566cc9a5de1f31ea0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359660"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a><span data-ttu-id="b6e12-102">DropOnPageScale, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="b6e12-102">DropOnPageScale Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="b6e12-103">Contient le pourcentage auquel une forme est mise à l'échelle lorsqu'elle est glissée sur la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="b6e12-103">Contains the percentage by which a shape is scaled when dropped on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6e12-104">Remarques</span><span class="sxs-lookup"><span data-stu-id="b6e12-104">Remarks</span></span>

<span data-ttu-id="b6e12-105">Dans les deux cas suivants, Visio met à l'échelle les formes pour qu'elles apparaissent correctement sur la page de dessin :</span><span class="sxs-lookup"><span data-stu-id="b6e12-105">In the following two cases, Visio scales shapes so that they appear appropriately on the drawing page:</span></span>
  
- <span data-ttu-id="b6e12-106">lorsque des formes non mesurées sont glissées sur des dessins mis à l'échelle ;</span><span class="sxs-lookup"><span data-stu-id="b6e12-106">When unmeasured shapes are dropped onto scaled drawings.</span></span>
    
- <span data-ttu-id="b6e12-107">Lorsque des formes mesurées sont insérées sur des dessins non ajustés.</span><span class="sxs-lookup"><span data-stu-id="b6e12-107">When measured shapes are dropped onto unscaled drawings.</span></span>
    
<span data-ttu-id="b6e12-108">Le pourcentage dans la cellule DropOnPageScale indique le facteur par lequel Visio a ajusté la forme, soit vers le\>haut (100),\<soit vers le bas (100).</span><span class="sxs-lookup"><span data-stu-id="b6e12-108">The percentage in the DropOnPageScale cell indicates the factor by which Visio scaled the shape, either up (\>100) or down (\<100).</span></span> <span data-ttu-id="b6e12-109">Vous pouvez utiliser ce nombre comme facteur lorsque vous calculez des valeurs préprogrammées.</span><span class="sxs-lookup"><span data-stu-id="b6e12-109">You can use this number as a factor when calculating hard-coded values.</span></span> 
  
<span data-ttu-id="b6e12-110">Cette valeur est de 100 % pour les formes mesurées sur des dessins mis à l'échelle ou les formes non mesurées sur des dessins non mis à l'échelle.</span><span class="sxs-lookup"><span data-stu-id="b6e12-110">This value is 100% for measured shapes on scaled drawings or unmeasured shapes on unscaled drawings.</span></span> 
  
<span data-ttu-id="b6e12-111">Pour obtenir une référence à la cellule DropOnPageScale par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b6e12-111">To get a reference to the DropOnPageScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6e12-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b6e12-112">Cell name:</span></span>  <br/> | <span data-ttu-id="b6e12-113">DropOnPageScale</span><span class="sxs-lookup"><span data-stu-id="b6e12-113">DropOnPageScale</span></span>  <br/> |
   
<span data-ttu-id="b6e12-114">Pour obtenir une référence à la cellule DropOnPageScale à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b6e12-114">To get a reference to the DropOnPageScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6e12-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b6e12-115">Section index:</span></span>  <br/> |<span data-ttu-id="b6e12-116">**Définis**</span><span class="sxs-lookup"><span data-stu-id="b6e12-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b6e12-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b6e12-117">Row index:</span></span>  <br/> |<span data-ttu-id="b6e12-118">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="b6e12-118">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="b6e12-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b6e12-119">Cell index:</span></span>  <br/> |<span data-ttu-id="b6e12-120">**visObjDropOnPageScale**</span><span class="sxs-lookup"><span data-stu-id="b6e12-120">**visObjDropOnPageScale**</span></span> <br/> |
   

