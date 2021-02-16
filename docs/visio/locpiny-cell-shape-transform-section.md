---
title: LocPinY, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Représente la coordonnée y de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme. La formule par défaut permettant de déterminer LocPinY est la suivante :'
ms.openlocfilehash: e65bfec8fdcf2be1ee92c23b7afcb183c95ea9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410594"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="f3374-104">LocPinY, cellule (section Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="f3374-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="f3374-105">Représente la  *coordonnée y*  de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="f3374-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="f3374-106">La formule par défaut permettant de déterminer LocPinY est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f3374-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="f3374-107">= Hauteur \* 0,5</span><span class="sxs-lookup"><span data-stu-id="f3374-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f3374-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3374-108">Remarks</span></span>

<span data-ttu-id="f3374-109">Pour obtenir une référence à la cellule LocPinY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f3374-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f3374-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f3374-110">Cell name:</span></span>  <br/> | <span data-ttu-id="f3374-111">LocPinY</span><span class="sxs-lookup"><span data-stu-id="f3374-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="f3374-112">Pour obtenir une référence à la cellule LocPinY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f3374-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f3374-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f3374-113">Section index:</span></span>  <br/> |<span data-ttu-id="f3374-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f3374-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f3374-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f3374-115">Row index:</span></span>  <br/> |<span data-ttu-id="f3374-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="f3374-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="f3374-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f3374-117">Cell index:</span></span>  <br/> |<span data-ttu-id="f3374-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="f3374-118">**visXFormLocPinY**</span></span> <br/> |
   

