---
title: PageLineJumpDirX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Détermine la direction des déviations de trait pour les connecteurs dynamiques horizontaux de la page de dessin n'ayant pas de direction de déviation locale.
ms.openlocfilehash: d414313e98107790f9236c0afabdc5747c6a2a10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789207"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a><span data-ttu-id="1febe-103">PageLineJumpDirX, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="1febe-103">PageLineJumpDirX Cell (Page Layout Section)</span></span>

<span data-ttu-id="1febe-104">Détermine la direction des déviations de trait pour les connecteurs dynamiques horizontaux de la page de dessin n'ayant pas de direction de déviation locale.</span><span class="sxs-lookup"><span data-stu-id="1febe-104">Determines the direction of line jumps on horizontal dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="1febe-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="1febe-105">**Value**</span></span>|<span data-ttu-id="1febe-106">**Direction de déviation de trait**</span><span class="sxs-lookup"><span data-stu-id="1febe-106">**Line jump direction**</span></span>|<span data-ttu-id="1febe-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="1febe-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1febe-108">0</span><span class="sxs-lookup"><span data-stu-id="1febe-108">0</span></span>  <br/> | <span data-ttu-id="1febe-109">Par défaut ; à gauche ou paramètres de la page pour les formes</span><span class="sxs-lookup"><span data-stu-id="1febe-109">Default; left or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="1febe-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="1febe-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="1febe-111">1</span><span class="sxs-lookup"><span data-stu-id="1febe-111">1</span></span>  <br/> | <span data-ttu-id="1febe-112">Haut</span><span class="sxs-lookup"><span data-stu-id="1febe-112">Up</span></span>  <br/> |<span data-ttu-id="1febe-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="1febe-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="1febe-114">2</span><span class="sxs-lookup"><span data-stu-id="1febe-114">2</span></span>  <br/> | <span data-ttu-id="1febe-115">Bas</span><span class="sxs-lookup"><span data-stu-id="1febe-115">Down</span></span>  <br/> |<span data-ttu-id="1febe-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="1febe-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1febe-117">Note</span><span class="sxs-lookup"><span data-stu-id="1febe-117">Remarks</span></span>

<span data-ttu-id="1febe-118">Pour obtenir une référence à la cellule PageLineJumpDirX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="1febe-118">To get a reference to the PageLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1febe-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1febe-119">Cell name:</span></span>  <br/> | <span data-ttu-id="1febe-120">PageLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="1febe-120">PageLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="1febe-121">Pour obtenir une référence à la cellule PageLineJumpDirX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1febe-121">To get a reference to the PageLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1febe-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1febe-122">Section index:</span></span>  <br/> |<span data-ttu-id="1febe-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1febe-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1febe-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1febe-124">Row index:</span></span>  <br/> |<span data-ttu-id="1febe-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="1febe-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="1febe-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1febe-126">Cell index:</span></span>  <br/> |<span data-ttu-id="1febe-127">**visPLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="1febe-127">**visPLOJumpDirX**</span></span> <br/> |
   

