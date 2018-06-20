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
ms.openlocfilehash: 16f0bac8f139c0b03d7826ac377a964d15296dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789599"
---
# <a name="scratch-section"></a><span data-ttu-id="a7e9d-103">Scratch, section</span><span class="sxs-lookup"><span data-stu-id="a7e9d-103">Scratch Section</span></span>

<span data-ttu-id="a7e9d-104">Zone de travail dans laquelle vous pouvez entrer et tester des formules auxquelles d'autres cellules sont susceptibles de faire référence.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7e9d-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7e9d-105">Remarks</span></span>

<span data-ttu-id="a7e9d-106">Vous pouvez ajouter cette section à l’aide de la boîte de dialogue **Insérer une Section** .</span><span class="sxs-lookup"><span data-stu-id="a7e9d-106">You can add this section by using the **Insert Section** dialog box.</span></span> <span data-ttu-id="a7e9d-107">Avec le bouton droit dans la fenêtre feuille ShapeSheet, puis cliquez sur **Insérer une Section**.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-107">Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="a7e9d-108">La section **Scratch** est généralement utilisée pour isoler les calculs répétés.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="a7e9d-109">Si votre solution a un objectif bien précis, il est préférable d’utiliser une cellule dans la section **User-Defined Cells** pour des raisons de clarté, car les cellules utilisateur peuvent être nommés.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="a7e9d-110">Les cellules dans la section **Scratch** utilisent les unités de deux manières différentes.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="a7e9d-111">Les cellules X et Y utilisent les unités de dessin ; N’utilisez pas une cellules D à unités.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="a7e9d-112">(Dans le jargon les programmeurs C, les cellules X et Y sont « tapés » et cellules de A à D sont « void ».) Les cellules **Scratch X** et **Y de montage** sont souvent utilisées pour dériver les coordonnées *x* et *y* , telles que **PinX** et **PinY**ou les cellules X et Y d’une cellule de la section **Geometry** .</span><span class="sxs-lookup"><span data-stu-id="a7e9d-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="a7e9d-113">Les cellules de montage Qu'a à D peut afficher toute unité que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="a7e9d-114">Une différence supplémentaire est la façon dont ces cellules stockent les valeurs de points.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="a7e9d-115">Un point dans Visio est un ensemble de données unique pour une coordonnée ( *x, y*).</span><span class="sxs-lookup"><span data-stu-id="a7e9d-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="a7e9d-116">Lorsqu’une formule renvoie une valeur de point, cette valeur est interprétée dans une des trois manières, selon la formule est dans la cellule de feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="a7e9d-117">Les cellules qui sont associées à *x* -coordonnées (par exemple, **PinX**ou les cellules dans la colonne X d’une section **Geometry** ) extrayez simplement le *x* -coordonner la partie d’une valeur en points.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="a7e9d-118">Les cellules liées à *y* -coordonnées extrayez simplement la valeur *y* -coordonner la partie d’une valeur en points.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="a7e9d-119">Par exemple, Visio extrait la formule `PNT(3,4)` ces trois manières.</span><span class="sxs-lookup"><span data-stu-id="a7e9d-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="a7e9d-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a7e9d-120">**Cell**</span></span>|<span data-ttu-id="a7e9d-121">**Si vous entrez**</span><span class="sxs-lookup"><span data-stu-id="a7e9d-121">**If you enter**</span></span>|<span data-ttu-id="a7e9d-122">**Visio la traite en tant que**</span><span class="sxs-lookup"><span data-stu-id="a7e9d-122">**Visio treats it as**</span></span>|<span data-ttu-id="a7e9d-123">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="a7e9d-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a7e9d-124">X </span><span class="sxs-lookup"><span data-stu-id="a7e9d-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="a7e9d-125">76,2000 mm</span><span class="sxs-lookup"><span data-stu-id="a7e9d-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="a7e9d-126">Y</span><span class="sxs-lookup"><span data-stu-id="a7e9d-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="a7e9d-127">4,0000 po</span><span class="sxs-lookup"><span data-stu-id="a7e9d-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="a7e9d-128">A-D</span><span class="sxs-lookup"><span data-stu-id="a7e9d-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="a7e9d-129">PNT (3.0000 pouces, 4.0000 in.)</span><span class="sxs-lookup"><span data-stu-id="a7e9d-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

