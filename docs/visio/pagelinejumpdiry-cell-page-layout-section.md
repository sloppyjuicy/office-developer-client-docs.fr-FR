---
title: PageLineJumpDirY, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Détermine la direction des déviations de trait pour les connecteurs dynamiques verticaux de la page de dessin n'ayant pas de direction de déviation locale.
ms.openlocfilehash: 21ad1d95fd83780f31778dbc8bb70f9bdb4b922d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414675"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a><span data-ttu-id="f8fbb-103">PageLineJumpDirY Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="f8fbb-103">PageLineJumpDirY Cell (Page Layout Section)</span></span>

<span data-ttu-id="f8fbb-104">Détermine la direction des déviations de trait pour les connecteurs dynamiques verticaux de la page de dessin n'ayant pas de direction de déviation locale.</span><span class="sxs-lookup"><span data-stu-id="f8fbb-104">Determines the direction of line jumps on vertical dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="f8fbb-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f8fbb-105">**Value**</span></span>|<span data-ttu-id="f8fbb-106">**Direction du saut de ligne**</span><span class="sxs-lookup"><span data-stu-id="f8fbb-106">**Line jump direction**</span></span>|<span data-ttu-id="f8fbb-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="f8fbb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f8fbb-108">0</span><span class="sxs-lookup"><span data-stu-id="f8fbb-108">0</span></span>  <br/> | <span data-ttu-id="f8fbb-109">Par défaut ; vers le haut ou paramètres de la page pour les formes</span><span class="sxs-lookup"><span data-stu-id="f8fbb-109">Default; up or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="f8fbb-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="f8fbb-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="f8fbb-111">1</span><span class="sxs-lookup"><span data-stu-id="f8fbb-111">1</span></span>  <br/> | <span data-ttu-id="f8fbb-112">À gauche</span><span class="sxs-lookup"><span data-stu-id="f8fbb-112">Left</span></span>  <br/> |<span data-ttu-id="f8fbb-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="f8fbb-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="f8fbb-114">2</span><span class="sxs-lookup"><span data-stu-id="f8fbb-114">2</span></span>  <br/> | <span data-ttu-id="f8fbb-115">À droite</span><span class="sxs-lookup"><span data-stu-id="f8fbb-115">Right</span></span>  <br/> |<span data-ttu-id="f8fbb-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="f8fbb-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8fbb-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="f8fbb-117">Remarks</span></span>

<span data-ttu-id="f8fbb-118">Pour obtenir une référence à la cellule PageLineJumpDirY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f8fbb-118">To get a reference to the PageLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8fbb-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f8fbb-119">Cell name:</span></span>  <br/> | <span data-ttu-id="f8fbb-120">PageLineJumpDiry</span><span class="sxs-lookup"><span data-stu-id="f8fbb-120">PageLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="f8fbb-121">Pour obtenir une référence à la cellule PageLineJumpDirY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f8fbb-121">To get a reference to the PageLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8fbb-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f8fbb-122">Section index:</span></span>  <br/> |<span data-ttu-id="f8fbb-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f8fbb-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f8fbb-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f8fbb-124">Row index:</span></span>  <br/> |<span data-ttu-id="f8fbb-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="f8fbb-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="f8fbb-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f8fbb-126">Cell index:</span></span>  <br/> |<span data-ttu-id="f8fbb-127">**visPLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="f8fbb-127">**visPLOJumpDirY**</span></span> <br/> |
   

