---
title: Scratch, section
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
localization_priority: Normal
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.
ms.openlocfilehash: a7d2c6762e96fc19986521c2ba164666b925c928
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411602"
---
# <a name="scratch-section"></a><span data-ttu-id="0465e-103">Scratch Section</span><span class="sxs-lookup"><span data-stu-id="0465e-103">Scratch Section</span></span>

<span data-ttu-id="0465e-104">Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.</span><span class="sxs-lookup"><span data-stu-id="0465e-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0465e-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="0465e-105">Remarks</span></span>

<span data-ttu-id="0465e-p101">Vous pouvez ajouter cette section à l’aide de la boîte de dialogue **Insérer une section**. Cliquez avec le bouton droit dans la fenêtre Feuille ShapeSheet, puis cliquez sur **Insérer une section**.</span><span class="sxs-lookup"><span data-stu-id="0465e-p101">You can add this section by using the **Insert Section** dialog box. Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="0465e-108">La section **Scratch** est généralement utilisée pour isoler les calculs complexes répétés.</span><span class="sxs-lookup"><span data-stu-id="0465e-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="0465e-109">Si votre solution a un objectif bien défini, il est plus judicieux d’utiliser une cellule dans la section **Cellules** définies par l’utilisateur pour plus de clarté, car les cellules utilisateur peuvent être nommées.</span><span class="sxs-lookup"><span data-stu-id="0465e-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="0465e-110">Les cellules de la section **Scratch** utilisent les unités de deux manières différentes.</span><span class="sxs-lookup"><span data-stu-id="0465e-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="0465e-111">Les cellules X et Y utilisent les unités de dessin ; les cellules de A à D n’utilisent pas d’unité.</span><span class="sxs-lookup"><span data-stu-id="0465e-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="0465e-112">(Dans le jargon des programmeurs en C, les cellules X et Y sont « typées » et les cellules A à D sont « vides ». Les cellules Scratch **X** et **Scratch Y** sont souvent utilisées pour dériver des coordonnées *x* et *y,* telles que **PinX** et **PinY,** ou les cellules X et Y trouvées dans une cellule de section **Geometry.**</span><span class="sxs-lookup"><span data-stu-id="0465e-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="0465e-113">Les cellules Scratch de A à D peuvent afficher toute unité que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="0465e-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="0465e-114">L'autre différence entre ces cellules tient à la façon dont les valeurs des points sont stockées.</span><span class="sxs-lookup"><span data-stu-id="0465e-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="0465e-115">Un point dans Visio est un package de données unique pour une coordonnée ( *x,y).*</span><span class="sxs-lookup"><span data-stu-id="0465e-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="0465e-116">Lorsqu'une formule renvoie une valeur de point, cette valeur est interprétée selon l'une des trois méthodes, suivant la cellule ShapeSheet dans laquelle se trouve la formule.</span><span class="sxs-lookup"><span data-stu-id="0465e-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="0465e-117">Les cellules liées aux coordonnées  *x*  (par exemple, **PinX** ou les cellules de la colonne X d’une section **Geometry)** extraient uniquement la partie coordonnée  *x*  d’une valeur de point.</span><span class="sxs-lookup"><span data-stu-id="0465e-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="0465e-118">Les cellules liées aux  *coordonnées y*  extraient uniquement la partie  *coordonnée y*  d’une valeur de point.</span><span class="sxs-lookup"><span data-stu-id="0465e-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="0465e-119">Par exemple, Visio extrait la formule `PNT(3,4)` de ces trois manières.</span><span class="sxs-lookup"><span data-stu-id="0465e-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="0465e-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="0465e-120">**Cell**</span></span>|<span data-ttu-id="0465e-121">**Si vous entrez**</span><span class="sxs-lookup"><span data-stu-id="0465e-121">**If you enter**</span></span>|<span data-ttu-id="0465e-122">**Visio la traite en tant que**</span><span class="sxs-lookup"><span data-stu-id="0465e-122">**Visio treats it as**</span></span>|<span data-ttu-id="0465e-123">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="0465e-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0465e-124">X</span><span class="sxs-lookup"><span data-stu-id="0465e-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="0465e-125">76,2000 mm</span><span class="sxs-lookup"><span data-stu-id="0465e-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="0465e-126">v</span><span class="sxs-lookup"><span data-stu-id="0465e-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="0465e-127">4,0000 po</span><span class="sxs-lookup"><span data-stu-id="0465e-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="0465e-128">A-D</span><span class="sxs-lookup"><span data-stu-id="0465e-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="0465e-129">PNT(3,0000, 4,0000 »)</span><span class="sxs-lookup"><span data-stu-id="0465e-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

