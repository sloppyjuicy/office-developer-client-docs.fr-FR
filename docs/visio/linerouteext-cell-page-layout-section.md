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
ms.openlocfilehash: 21da283f2d9ab43837b8fe4127840e89ea9d9949
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788970"
---
# <a name="linerouteext-cell-page-layout-section"></a><span data-ttu-id="5145b-103">LineRouteExt, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="5145b-103">LineRouteExt Cell (Page Layout Section)</span></span>

<span data-ttu-id="5145b-104">Détermine l'aspect par défaut de tous les connecteurs d'une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="5145b-104">Determines the default appearance for all connectors on a drawing page.</span></span>
  
|<span data-ttu-id="5145b-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5145b-105">**Value**</span></span>|<span data-ttu-id="5145b-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="5145b-106">**Description**</span></span>|<span data-ttu-id="5145b-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="5145b-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="5145b-108">0</span><span class="sxs-lookup"><span data-stu-id="5145b-108">0</span></span>  <br/> | <span data-ttu-id="5145b-109">Par défaut (droit)</span><span class="sxs-lookup"><span data-stu-id="5145b-109">Default (straight)</span></span>  <br/> |<span data-ttu-id="5145b-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="5145b-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="5145b-111">1</span><span class="sxs-lookup"><span data-stu-id="5145b-111">1</span></span>  <br/> | <span data-ttu-id="5145b-112">Droit</span><span class="sxs-lookup"><span data-stu-id="5145b-112">Straight</span></span>  <br/> |<span data-ttu-id="5145b-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="5145b-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="5145b-114">2</span><span class="sxs-lookup"><span data-stu-id="5145b-114">2</span></span>  <br/> | <span data-ttu-id="5145b-115">Courbé</span><span class="sxs-lookup"><span data-stu-id="5145b-115">Curved</span></span>  <br/> |<span data-ttu-id="5145b-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="5145b-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5145b-117">Note</span><span class="sxs-lookup"><span data-stu-id="5145b-117">Remarks</span></span>

<span data-ttu-id="5145b-118">Pour obtenir une référence à la cellule LineRouteExt par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="5145b-118">To get a reference to the LineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5145b-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5145b-119">Cell name:</span></span>  <br/> | <span data-ttu-id="5145b-120">LineRouteExt</span><span class="sxs-lookup"><span data-stu-id="5145b-120">LineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="5145b-121">Pour obtenir une référence à la cellule LineRouteExt par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5145b-121">To get a reference to the LineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5145b-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5145b-122">Section index:</span></span>  <br/> |<span data-ttu-id="5145b-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5145b-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5145b-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5145b-124">Row index:</span></span>  <br/> |<span data-ttu-id="5145b-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="5145b-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="5145b-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5145b-126">Cell index:</span></span>  <br/> |<span data-ttu-id="5145b-127">**visPLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="5145b-127">**visPLOLineRouteExt**</span></span> <br/> |
   

