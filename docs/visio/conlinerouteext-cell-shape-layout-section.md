---
title: ConLineRouteExt, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Détermine l'aspect d'un connecteur.
ms.openlocfilehash: 19fe948daf7aa3d67db858849ecb2b15f40ba02d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434612"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a><span data-ttu-id="7dbd3-103">ConLineRouteExt, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="7dbd3-103">ConLineRouteExt Cell (Shape Layout Section)</span></span>

<span data-ttu-id="7dbd3-104">Détermine l'aspect d'un connecteur.</span><span class="sxs-lookup"><span data-stu-id="7dbd3-104">Determines the appearance of a connector.</span></span>
  
|<span data-ttu-id="7dbd3-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7dbd3-105">**Value**</span></span>|<span data-ttu-id="7dbd3-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="7dbd3-106">**Description**</span></span>|<span data-ttu-id="7dbd3-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="7dbd3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7dbd3-108">0</span><span class="sxs-lookup"><span data-stu-id="7dbd3-108">0</span></span>  <br/> | <span data-ttu-id="7dbd3-109">Valeur par défaut ; utilise le paramètre de la page</span><span class="sxs-lookup"><span data-stu-id="7dbd3-109">Default; use page setting</span></span>  <br/> |<span data-ttu-id="7dbd3-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="7dbd3-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="7dbd3-111">1</span><span class="sxs-lookup"><span data-stu-id="7dbd3-111">1</span></span>  <br/> | <span data-ttu-id="7dbd3-112">Droite</span><span class="sxs-lookup"><span data-stu-id="7dbd3-112">Straight</span></span>  <br/> |<span data-ttu-id="7dbd3-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="7dbd3-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="7dbd3-114">2</span><span class="sxs-lookup"><span data-stu-id="7dbd3-114">2</span></span>  <br/> | <span data-ttu-id="7dbd3-115">Courbe</span><span class="sxs-lookup"><span data-stu-id="7dbd3-115">Curved</span></span>  <br/> |<span data-ttu-id="7dbd3-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="7dbd3-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7dbd3-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="7dbd3-117">Remarks</span></span>

<span data-ttu-id="7dbd3-118">Pour obtenir une référence à la cellule ConLineTouteExt par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7dbd3-118">To get a reference to the ConLineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7dbd3-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7dbd3-119">Cell name:</span></span>  <br/> | <span data-ttu-id="7dbd3-120">ConLineRouteExt</span><span class="sxs-lookup"><span data-stu-id="7dbd3-120">ConLineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="7dbd3-121">Pour obtenir une référence à la cellule ConLineRouteExt à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7dbd3-121">To get a reference to the ConLineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7dbd3-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7dbd3-122">Section index:</span></span>  <br/> |<span data-ttu-id="7dbd3-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7dbd3-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7dbd3-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7dbd3-124">Row index:</span></span>  <br/> |<span data-ttu-id="7dbd3-125">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="7dbd3-125">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="7dbd3-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7dbd3-126">Cell index:</span></span>  <br/> |<span data-ttu-id="7dbd3-127">**visSLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="7dbd3-127">**visSLOLineRouteExt**</span></span> <br/> |
   

