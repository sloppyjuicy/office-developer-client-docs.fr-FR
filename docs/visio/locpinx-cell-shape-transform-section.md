---
title: LocPinX, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: "Représente la coordonnée x de l'axe de la forme (Centre de rotation) par rapport à l'origine de la forme. La formule par défaut permettant de déterminer LocPinX est la suivante :"
ms.openlocfilehash: 2eb5c328eed3c97652173670c426b83b8c358833
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439239"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="6d3f8-104">LocPinX, cellule (section Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="6d3f8-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="6d3f8-105">Représente la coordonnée *x* de l'axe de la forme (Centre de rotation) par rapport à l'origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="6d3f8-106">La formule par défaut permettant de déterminer LocPinX est la suivante :</span><span class="sxs-lookup"><span data-stu-id="6d3f8-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="6d3f8-107">= Largeur \* 0,5</span><span class="sxs-lookup"><span data-stu-id="6d3f8-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d3f8-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d3f8-108">Remarks</span></span>

<span data-ttu-id="6d3f8-109">Pour obtenir une référence à la cellule LocPinX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="6d3f8-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d3f8-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6d3f8-110">Cell name:</span></span>  <br/> | <span data-ttu-id="6d3f8-111">LocPinX</span><span class="sxs-lookup"><span data-stu-id="6d3f8-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="6d3f8-112">Pour obtenir une référence à la cellule LocPinX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="6d3f8-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d3f8-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6d3f8-113">Section index:</span></span>  <br/> |<span data-ttu-id="6d3f8-114">**Définis**</span><span class="sxs-lookup"><span data-stu-id="6d3f8-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6d3f8-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6d3f8-115">Row index:</span></span>  <br/> |<span data-ttu-id="6d3f8-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="6d3f8-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="6d3f8-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6d3f8-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6d3f8-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="6d3f8-118">**visXFormLocPinX**</span></span> <br/> |
   

