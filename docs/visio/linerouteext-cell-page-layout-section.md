---
title: LineRouteExt, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Détermine l'aspect par défaut de tous les connecteurs d'une page de dessin.
ms.openlocfilehash: 6daed2e06f7673e5a4ec97ec83dc31bad2766301
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410622"
---
# <a name="linerouteext-cell-page-layout-section"></a><span data-ttu-id="30a3e-103">LineRouteExt, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="30a3e-103">LineRouteExt Cell (Page Layout Section)</span></span>

<span data-ttu-id="30a3e-104">Détermine l'aspect par défaut de tous les connecteurs d'une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="30a3e-104">Determines the default appearance for all connectors on a drawing page.</span></span>
  
|<span data-ttu-id="30a3e-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="30a3e-105">**Value**</span></span>|<span data-ttu-id="30a3e-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="30a3e-106">**Description**</span></span>|<span data-ttu-id="30a3e-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="30a3e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="30a3e-108">0</span><span class="sxs-lookup"><span data-stu-id="30a3e-108">0</span></span>  <br/> | <span data-ttu-id="30a3e-109">Par défaut (droit)</span><span class="sxs-lookup"><span data-stu-id="30a3e-109">Default (straight)</span></span>  <br/> |<span data-ttu-id="30a3e-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="30a3e-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="30a3e-111">1 </span><span class="sxs-lookup"><span data-stu-id="30a3e-111">1</span></span>  <br/> | <span data-ttu-id="30a3e-112">Droite</span><span class="sxs-lookup"><span data-stu-id="30a3e-112">Straight</span></span>  <br/> |<span data-ttu-id="30a3e-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="30a3e-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="30a3e-114">2 </span><span class="sxs-lookup"><span data-stu-id="30a3e-114">2</span></span>  <br/> | <span data-ttu-id="30a3e-115">Courbe</span><span class="sxs-lookup"><span data-stu-id="30a3e-115">Curved</span></span>  <br/> |<span data-ttu-id="30a3e-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="30a3e-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30a3e-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="30a3e-117">Remarks</span></span>

<span data-ttu-id="30a3e-118">Pour obtenir une référence à la cellule LineRouteExt par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="30a3e-118">To get a reference to the LineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30a3e-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="30a3e-119">Cell name:</span></span>  <br/> | <span data-ttu-id="30a3e-120">LineRouteExt</span><span class="sxs-lookup"><span data-stu-id="30a3e-120">LineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="30a3e-121">Pour obtenir une référence à la cellule LineRouteExt à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="30a3e-121">To get a reference to the LineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30a3e-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="30a3e-122">Section index:</span></span>  <br/> |<span data-ttu-id="30a3e-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="30a3e-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="30a3e-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="30a3e-124">Row index:</span></span>  <br/> |<span data-ttu-id="30a3e-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="30a3e-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="30a3e-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="30a3e-126">Cell index:</span></span>  <br/> |<span data-ttu-id="30a3e-127">**visPLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="30a3e-127">**visPLOLineRouteExt**</span></span> <br/> |
   

