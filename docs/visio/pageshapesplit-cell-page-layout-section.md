---
title: PageShapeSplit, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Indique si les formes de la page peuvent être fractionnées automatiquement.
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301483"
---
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="189b7-103">PageShapeSplit, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="189b7-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="189b7-104">Indique si les formes de la page peuvent être fractionnées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="189b7-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="189b7-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="189b7-105">**Value**</span></span>|<span data-ttu-id="189b7-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="189b7-106">**Description**</span></span>|<span data-ttu-id="189b7-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="189b7-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="189b7-108">0</span><span class="sxs-lookup"><span data-stu-id="189b7-108">0</span></span>  <br/> |<span data-ttu-id="189b7-109">Ne pas autoriser le fractionnement automatique des formes.</span><span class="sxs-lookup"><span data-stu-id="189b7-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="189b7-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="189b7-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="189b7-111">0,1</span><span class="sxs-lookup"><span data-stu-id="189b7-111">1</span></span>  <br/> |<span data-ttu-id="189b7-112">Autoriser le fractionnement automatique des formes (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="189b7-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="189b7-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="189b7-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="189b7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="189b7-114">Remarks</span></span>

<span data-ttu-id="189b7-p101">Le fractionnement automatique des formes est activé et désactivé à trois niveaux différents : application, page et forme. Par défaut, le fractionnement est activé aux niveaux application et page. Le paramètre par défaut pour les formes varie en fonction du type de dessin.</span><span class="sxs-lookup"><span data-stu-id="189b7-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page levels. The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="189b7-118">Pour activer ou désactiver le fractionnement au niveau de l'application, utilisez le paramètre autoriser le fractionnement des **liens** sous l'onglet **avancé** de la boîte de dialogue **options Visio** (cliquez sur le bouton **Office** , cliquez sur **options** dans **Visio** , puis cliquez sur **avancé** .</span><span class="sxs-lookup"><span data-stu-id="189b7-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="189b7-119">Pour activer ou désactiver le fractionnement au niveau de la forme, reportez-vous aux cellules ShapeSplit et ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="189b7-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="189b7-120">Pour obtenir une référence à la cellule PageShapeSplit par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="189b7-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="189b7-121">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="189b7-121">Cell name:</span></span>  <br/> |<span data-ttu-id="189b7-122">PageShapeSplit</span><span class="sxs-lookup"><span data-stu-id="189b7-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="189b7-123">Pour obtenir une référence à la cellule PageShapeSplit à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="189b7-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="189b7-124">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="189b7-124">Section index:</span></span>  <br/> |<span data-ttu-id="189b7-125">**Définis**</span><span class="sxs-lookup"><span data-stu-id="189b7-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="189b7-126">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="189b7-126">Row index:</span></span>  <br/> |<span data-ttu-id="189b7-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="189b7-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="189b7-128">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="189b7-128">Cell index:</span></span>  <br/> |<span data-ttu-id="189b7-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="189b7-129">**visPLOSplit**</span></span> <br/> |
   

