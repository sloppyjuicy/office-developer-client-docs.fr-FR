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
ms.openlocfilehash: 9f92cf7d147be8e59d860bcc8a958bf0cdc008c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427072"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="23f15-103">ShapeSplittable, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="23f15-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="23f15-104">Indique si cette forme 1D peut être fractionnée.</span><span class="sxs-lookup"><span data-stu-id="23f15-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="23f15-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="23f15-105">**Value**</span></span>|<span data-ttu-id="23f15-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="23f15-106">**Description**</span></span>|<span data-ttu-id="23f15-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="23f15-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="23f15-108">0</span><span class="sxs-lookup"><span data-stu-id="23f15-108">0</span></span>  <br/> | <span data-ttu-id="23f15-109">Ne pas autoriser cette forme à être fractionnée.</span><span class="sxs-lookup"><span data-stu-id="23f15-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="23f15-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="23f15-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="23f15-111">1 </span><span class="sxs-lookup"><span data-stu-id="23f15-111">1</span></span>  <br/> | <span data-ttu-id="23f15-112">Autoriser cette forme à être fractionnée.</span><span class="sxs-lookup"><span data-stu-id="23f15-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="23f15-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="23f15-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23f15-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="23f15-114">Remarks</span></span>

<span data-ttu-id="23f15-115">Le comportement par défaut des connecteurs et autres formes 1D varie en fonction du type de dessin.</span><span class="sxs-lookup"><span data-stu-id="23f15-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="23f15-p101">Le fractionnement automatique des formes est activé et désactivé à trois niveaux différents : application, page et forme. Par défaut, le fractionnement est activé aux niveaux de l’application et de la page.</span><span class="sxs-lookup"><span data-stu-id="23f15-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="23f15-118">Pour activer ou désactiver le fractionnement  au niveau de  l’application, utilisez le paramètre Activer  le fractionnement de connecteur sous l’onglet Avancé de la boîte de dialogue **Options Visio** (cliquez sur l’onglet Fichier, sur **Options,** puis sur **Options** avancées).</span><span class="sxs-lookup"><span data-stu-id="23f15-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="23f15-119">Pour activer ou désactiver le fractionnement sur une page, consultez la rubrique de la cellule [PageShapeSplit](pageshapesplit-cell-page-layout-section.md).</span><span class="sxs-lookup"><span data-stu-id="23f15-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="23f15-120">Pour savoir comment une forme peut fractionner les formes 1D fractionnables, consultez la rubrique de la cellule [ShapeSplit](shapesplit-cell-shape-layout-section.md).</span><span class="sxs-lookup"><span data-stu-id="23f15-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="23f15-121">Pour obtenir une référence à la cellule ShapeSplittable par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="23f15-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23f15-122">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="23f15-122">Cell name:</span></span>  <br/> | <span data-ttu-id="23f15-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="23f15-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="23f15-124">Pour obtenir une référence à la cellule ShapeSplittable à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="23f15-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23f15-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="23f15-125">Section index:</span></span>  <br/> |<span data-ttu-id="23f15-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="23f15-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="23f15-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="23f15-127">Row index:</span></span>  <br/> |<span data-ttu-id="23f15-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="23f15-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="23f15-129">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="23f15-129">Cell index:</span></span>  <br/> |<span data-ttu-id="23f15-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="23f15-130">**visSLOSplittable**</span></span> <br/> |
   

