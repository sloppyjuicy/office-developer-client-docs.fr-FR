---
title: ShapeSplit, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Indique si cette forme peut fractionner les formes fractionnables.
ms.openlocfilehash: 46b42e9be070b54095d3e9a5c247d63be6348f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423558"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="c0514-103">ShapeSplit, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="c0514-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="c0514-104">Indique si cette forme peut fractionner les formes fractionnables.</span><span class="sxs-lookup"><span data-stu-id="c0514-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="c0514-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c0514-105">**Value**</span></span>|<span data-ttu-id="c0514-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0514-106">**Description**</span></span>|<span data-ttu-id="c0514-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="c0514-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c0514-108">0</span><span class="sxs-lookup"><span data-stu-id="c0514-108">0</span></span>  <br/> | <span data-ttu-id="c0514-109">Ne pas autoriser cette forme à en fractionner d’autres.</span><span class="sxs-lookup"><span data-stu-id="c0514-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="c0514-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="c0514-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="c0514-111">0,1</span><span class="sxs-lookup"><span data-stu-id="c0514-111">1</span></span>  <br/> | <span data-ttu-id="c0514-112">Autoriser cette forme à en fractionner d’autres.</span><span class="sxs-lookup"><span data-stu-id="c0514-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="c0514-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="c0514-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0514-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0514-114">Remarks</span></span>

<span data-ttu-id="c0514-115">Une forme qui peut en fractionner d’autres doit être une forme 2D ou une forme 1D positionnable.</span><span class="sxs-lookup"><span data-stu-id="c0514-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="c0514-p101">Le fractionnement automatique des formes est activé et désactivé à trois niveaux différents : application, page et forme. Par défaut, le fractionnement est activé aux niveaux application et page ; pour les formes, il varie en fonction du type de dessin.</span><span class="sxs-lookup"><span data-stu-id="c0514-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="c0514-118">Pour activer ou désactiver le fractionnement au niveau de l'application, utilisez le paramètre autoriser le fractionnement des **liens** sous l'onglet options **avancées** de la boîte de dialogue **options Visio** (cliquez sur l'onglet **fichier** , sur **options**, puis sur \*\* Avancé\*\*).</span><span class="sxs-lookup"><span data-stu-id="c0514-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="c0514-119">Pour activer ou désactiver le fractionnement sur une page, reportez-vous à la cellule PageShapeSplit.</span><span class="sxs-lookup"><span data-stu-id="c0514-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="c0514-120">Pour rendre une forme 1D fractionnable, reportez-vous à la cellule ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="c0514-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="c0514-121">Pour obtenir une référence à la cellule ShapeSplit par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="c0514-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0514-122">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="c0514-122">Cell name:</span></span>  <br/> | <span data-ttu-id="c0514-123">ShapeSplit</span><span class="sxs-lookup"><span data-stu-id="c0514-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="c0514-124">Pour obtenir une référence à la cellule ShapeSplit à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c0514-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c0514-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c0514-125">Section index:</span></span>  <br/> |<span data-ttu-id="c0514-126">**Définis**</span><span class="sxs-lookup"><span data-stu-id="c0514-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c0514-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c0514-127">Row index:</span></span>  <br/> |<span data-ttu-id="c0514-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="c0514-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="c0514-129">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c0514-129">Cell index:</span></span>  <br/> |<span data-ttu-id="c0514-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="c0514-130">**visSLOSplit**</span></span> <br/> |
   

