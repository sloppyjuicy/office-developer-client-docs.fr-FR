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
ms.openlocfilehash: 640ad93fbccf2cec26bda535c288c881aea32207
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789218"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a><span data-ttu-id="f3e00-103">PageLineJumpDirY, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="f3e00-103">PageLineJumpDirY Cell (Page Layout Section)</span></span>

<span data-ttu-id="f3e00-104">Détermine la direction des déviations de trait pour les connecteurs dynamiques verticaux de la page de dessin n'ayant pas de direction de déviation locale.</span><span class="sxs-lookup"><span data-stu-id="f3e00-104">Determines the direction of line jumps on vertical dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="f3e00-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f3e00-105">**Value**</span></span>|<span data-ttu-id="f3e00-106">**Direction de déviation de trait**</span><span class="sxs-lookup"><span data-stu-id="f3e00-106">**Line jump direction**</span></span>|<span data-ttu-id="f3e00-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="f3e00-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f3e00-108">0</span><span class="sxs-lookup"><span data-stu-id="f3e00-108">0</span></span>  <br/> | <span data-ttu-id="f3e00-109">Par défaut ; vers le haut ou paramètres de la page pour les formes</span><span class="sxs-lookup"><span data-stu-id="f3e00-109">Default; up or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="f3e00-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="f3e00-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="f3e00-111">1</span><span class="sxs-lookup"><span data-stu-id="f3e00-111">1</span></span>  <br/> | <span data-ttu-id="f3e00-112">Gauche</span><span class="sxs-lookup"><span data-stu-id="f3e00-112">Left</span></span>  <br/> |<span data-ttu-id="f3e00-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="f3e00-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="f3e00-114">2</span><span class="sxs-lookup"><span data-stu-id="f3e00-114">2</span></span>  <br/> | <span data-ttu-id="f3e00-115">Droite</span><span class="sxs-lookup"><span data-stu-id="f3e00-115">Right</span></span>  <br/> |<span data-ttu-id="f3e00-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="f3e00-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3e00-117">Note</span><span class="sxs-lookup"><span data-stu-id="f3e00-117">Remarks</span></span>

<span data-ttu-id="f3e00-118">Pour obtenir une référence à la cellule PageLineJumpDirY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="f3e00-118">To get a reference to the PageLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f3e00-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f3e00-119">Cell name:</span></span>  <br/> | <span data-ttu-id="f3e00-120">PageLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="f3e00-120">PageLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="f3e00-121">Pour obtenir une référence à la cellule PageLineJumpDirY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f3e00-121">To get a reference to the PageLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f3e00-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f3e00-122">Section index:</span></span>  <br/> |<span data-ttu-id="f3e00-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f3e00-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f3e00-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f3e00-124">Row index:</span></span>  <br/> |<span data-ttu-id="f3e00-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="f3e00-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="f3e00-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f3e00-126">Cell index:</span></span>  <br/> |<span data-ttu-id="f3e00-127">**visPLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="f3e00-127">**visPLOJumpDirY**</span></span> <br/> |
   

