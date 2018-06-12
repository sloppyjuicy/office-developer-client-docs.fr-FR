---
title: ShapeSplittable, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Indique si cette forme 1D peut être fractionnée.
ms.openlocfilehash: e2db881465a19b34d5788f1621f15c4d7d15c293
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789681"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="53f5d-103">ShapeSplittable, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="53f5d-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="53f5d-104">Indique si cette forme 1D peut être fractionnée.</span><span class="sxs-lookup"><span data-stu-id="53f5d-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="53f5d-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="53f5d-105">**Value**</span></span>|<span data-ttu-id="53f5d-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="53f5d-106">**Description**</span></span>|<span data-ttu-id="53f5d-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="53f5d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="53f5d-108">0</span><span class="sxs-lookup"><span data-stu-id="53f5d-108">0</span></span>  <br/> | <span data-ttu-id="53f5d-109">Ne pas autoriser cette forme à être fractionnée.</span><span class="sxs-lookup"><span data-stu-id="53f5d-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="53f5d-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="53f5d-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="53f5d-111">1</span><span class="sxs-lookup"><span data-stu-id="53f5d-111">1</span></span>  <br/> | <span data-ttu-id="53f5d-112">Autoriser cette forme à être fractionnée.</span><span class="sxs-lookup"><span data-stu-id="53f5d-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="53f5d-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="53f5d-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53f5d-114">Note</span><span class="sxs-lookup"><span data-stu-id="53f5d-114">Remarks</span></span>

<span data-ttu-id="53f5d-115">Le comportement par défaut des connecteurs et autres formes 1D varie en fonction du type de dessin.</span><span class="sxs-lookup"><span data-stu-id="53f5d-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="53f5d-p101">Le fractionnement automatique des formes est activé et désactivé à trois niveaux différents : application, page et forme. Par défaut, le fractionnement est activé aux niveaux de l’application et de la page.</span><span class="sxs-lookup"><span data-stu-id="53f5d-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="53f5d-118">Pour activer ou désactiver le fractionnement au niveau de l’application, utilisez le paramètre **Autoriser le fractionnement** sur l’onglet **Avancé** de la boîte de dialogue **Options Visio** (cliquez sur l’onglet **fichier** , cliquez sur **Options**, puis cliquez sur ** Avancés** ).</span><span class="sxs-lookup"><span data-stu-id="53f5d-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="53f5d-119">Pour activer ou désactiver le fractionnement sur une page, reportez-vous à la cellule [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) .</span><span class="sxs-lookup"><span data-stu-id="53f5d-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="53f5d-120">Pour qu’une forme peut fractionner les formes fractionnables 1-D, reportez-vous à la cellule [ShapeSplit](shapesplit-cell-shape-layout-section.md) .</span><span class="sxs-lookup"><span data-stu-id="53f5d-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="53f5d-121">Pour obtenir une référence à la cellule ShapleSplittable par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="53f5d-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="53f5d-122">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="53f5d-122">Cell name:</span></span>  <br/> | <span data-ttu-id="53f5d-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="53f5d-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="53f5d-124">Pour obtenir une référence à la cellule ShapeSplittable par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="53f5d-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="53f5d-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="53f5d-125">Section index:</span></span>  <br/> |<span data-ttu-id="53f5d-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="53f5d-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="53f5d-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="53f5d-127">Row index:</span></span>  <br/> |<span data-ttu-id="53f5d-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="53f5d-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="53f5d-129">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="53f5d-129">Cell index:</span></span>  <br/> |<span data-ttu-id="53f5d-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="53f5d-130">**visSLOSplittable**</span></span> <br/> |
   

