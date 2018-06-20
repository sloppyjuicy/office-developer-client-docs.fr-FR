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
description: 'Représente la valeur y-coordonnées de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme. La formule par défaut permettant de déterminer LocPinY est la suivante :'
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789035"
---
# <a name="locpiny-cell-shape-transform-section"></a><span data-ttu-id="50df8-104">LocPinY, cellule (section Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="50df8-104">LocPinY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="50df8-105">Représente la valeur *y* -coordonnées de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="50df8-105">Represents the  *y*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="50df8-106">La formule par défaut permettant de déterminer LocPinY est la suivante :</span><span class="sxs-lookup"><span data-stu-id="50df8-106">The default formula for determining LocPinY is:</span></span> 
  
<span data-ttu-id="50df8-107">= Hauteur \* 0,5</span><span class="sxs-lookup"><span data-stu-id="50df8-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50df8-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="50df8-108">Remarks</span></span>

<span data-ttu-id="50df8-109">Pour obtenir une référence à la cellule LocPinY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="50df8-109">To get a reference to the LocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50df8-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="50df8-110">Cell name:</span></span>  <br/> | <span data-ttu-id="50df8-111">LocPinY</span><span class="sxs-lookup"><span data-stu-id="50df8-111">LocPinY</span></span>  <br/> |
   
<span data-ttu-id="50df8-112">Pour obtenir une référence à la cellule LocPinY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="50df8-112">To get a reference to the LocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50df8-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="50df8-113">Section index:</span></span>  <br/> |<span data-ttu-id="50df8-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="50df8-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="50df8-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="50df8-115">Row index:</span></span>  <br/> |<span data-ttu-id="50df8-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="50df8-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="50df8-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="50df8-117">Cell index:</span></span>  <br/> |<span data-ttu-id="50df8-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="50df8-118">**visXFormLocPinY**</span></span> <br/> |
   

