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
description: 'Représente le x-coordonnées de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme. La formule par défaut permettant de déterminer LocPinX est la suivante :'
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789048"
---
# <a name="locpinx-cell-shape-transform-section"></a><span data-ttu-id="feb16-104">LocPinX, cellule (section Shape Transform)</span><span class="sxs-lookup"><span data-stu-id="feb16-104">LocPinX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="feb16-105">Représente le *x* -coordonnées de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="feb16-105">Represents the  *x*  -coordinate of the shape's pin (center of rotation) in relation to the origin of the shape.</span></span> <span data-ttu-id="feb16-106">La formule par défaut permettant de déterminer LocPinX est la suivante :</span><span class="sxs-lookup"><span data-stu-id="feb16-106">The default formula for determining LocPinX is:</span></span> 
  
<span data-ttu-id="feb16-107">= Largeur \* 0,5</span><span class="sxs-lookup"><span data-stu-id="feb16-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="feb16-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="feb16-108">Remarks</span></span>

<span data-ttu-id="feb16-109">Pour obtenir une référence à la cellule LocPinX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="feb16-109">To get a reference to the LocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="feb16-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="feb16-110">Cell name:</span></span>  <br/> | <span data-ttu-id="feb16-111">LocPinX</span><span class="sxs-lookup"><span data-stu-id="feb16-111">LocPinX</span></span>  <br/> |
   
<span data-ttu-id="feb16-112">Pour obtenir une référence à la cellule LocPinX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="feb16-112">To get a reference to the LocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="feb16-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="feb16-113">Section index:</span></span>  <br/> |<span data-ttu-id="feb16-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="feb16-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="feb16-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="feb16-115">Row index:</span></span>  <br/> |<span data-ttu-id="feb16-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="feb16-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="feb16-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="feb16-117">Cell index:</span></span>  <br/> |<span data-ttu-id="feb16-118">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="feb16-118">**visXFormLocPinX**</span></span> <br/> |
   

