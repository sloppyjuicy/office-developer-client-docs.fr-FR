---
title: ConLineJumpDirX, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Détermine la direction de la déviation du trait dans le cas d'un connecteur dynamique horizontal d'une forme.
ms.openlocfilehash: 22b9366b750a85a76498b83880aac2b9b974e1ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415039"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="1c77e-103">ConLineJumpDirX, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="1c77e-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="1c77e-104">Détermine la direction de la déviation du trait dans le cas d'un connecteur dynamique horizontal d'une forme.</span><span class="sxs-lookup"><span data-stu-id="1c77e-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="1c77e-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="1c77e-105">**Value**</span></span>|<span data-ttu-id="1c77e-106">**Direction du saut de ligne**</span><span class="sxs-lookup"><span data-stu-id="1c77e-106">**Line jump direction**</span></span>|<span data-ttu-id="1c77e-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="1c77e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1c77e-108">0</span><span class="sxs-lookup"><span data-stu-id="1c77e-108">0</span></span>  <br/> | <span data-ttu-id="1c77e-109">Valeur par défaut de la page</span><span class="sxs-lookup"><span data-stu-id="1c77e-109">Page default</span></span>  <br/> |<span data-ttu-id="1c77e-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="1c77e-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="1c77e-111">1 </span><span class="sxs-lookup"><span data-stu-id="1c77e-111">1</span></span>  <br/> | <span data-ttu-id="1c77e-112">Up</span><span class="sxs-lookup"><span data-stu-id="1c77e-112">Up</span></span>  <br/> |<span data-ttu-id="1c77e-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="1c77e-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="1c77e-114">2 </span><span class="sxs-lookup"><span data-stu-id="1c77e-114">2</span></span>  <br/> | <span data-ttu-id="1c77e-115">Down</span><span class="sxs-lookup"><span data-stu-id="1c77e-115">Down</span></span>  <br/> |<span data-ttu-id="1c77e-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="1c77e-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c77e-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c77e-117">Remarks</span></span>

<span data-ttu-id="1c77e-118">Pour définir l’orientation  horizontale par défaut pour tous les sauts de connecteur sur une page, utilisez la cellule PageLineJumpDirX dans la section Mise en page.</span><span class="sxs-lookup"><span data-stu-id="1c77e-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="1c77e-119">Pour obtenir une référence à la cellule ConLineJumpDirX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="1c77e-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c77e-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1c77e-120">Cell name:</span></span>  <br/> | <span data-ttu-id="1c77e-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="1c77e-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="1c77e-122">Pour obtenir une référence à la cellule ConLineJumpDirX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1c77e-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c77e-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1c77e-123">Section index:</span></span>  <br/> |<span data-ttu-id="1c77e-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1c77e-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1c77e-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1c77e-125">Row index:</span></span>  <br/> |<span data-ttu-id="1c77e-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="1c77e-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="1c77e-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1c77e-127">Cell index:</span></span>  <br/> |<span data-ttu-id="1c77e-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="1c77e-128">**visSLOJumpDirX**</span></span> <br/> |
   

