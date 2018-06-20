---
title: EnableGrid, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Détermine si l’application aligne les formes sur une grille de page interne invisible lorsque vous configurez la mise en page dans la boîte de dialogue Configurer la disposition. (Sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de disposition.)
ms.openlocfilehash: 3371767343132219ebc38134b93afd1da46c7a45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788551"
---
# <a name="enablegrid-cell-page-layout-section"></a><span data-ttu-id="8adef-104">EnableGrid, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="8adef-104">EnableGrid Cell (Page Layout Section)</span></span>

<span data-ttu-id="8adef-105">Détermine si l’application aligne les formes sur une grille de page interne invisible lorsque vous configurez la mise en page dans la boîte de dialogue **Configurer la disposition** .</span><span class="sxs-lookup"><span data-stu-id="8adef-105">Determines whether the application lays out shapes based on an internal, invisible page grid when you configure the layout in the **Configure Layout** dialog box.</span></span> <span data-ttu-id="8adef-106">(Sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur **Autres Options de disposition**.)</span><span class="sxs-lookup"><span data-stu-id="8adef-106">(On the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**.)</span></span>
  
|<span data-ttu-id="8adef-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8adef-107">**Value**</span></span>|<span data-ttu-id="8adef-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="8adef-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8adef-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="8adef-109">TRUE</span></span>  <br/> |<span data-ttu-id="8adef-110">Utilise la grille de page interne.</span><span class="sxs-lookup"><span data-stu-id="8adef-110">Use the internal page grid.</span></span>  <br/> |
|<span data-ttu-id="8adef-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="8adef-111">FALSE</span></span>  <br/> |<span data-ttu-id="8adef-112">N'utilise pas la grille de page interne.</span><span class="sxs-lookup"><span data-stu-id="8adef-112">Do not use the internal page grid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8adef-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="8adef-113">Remarks</span></span>

<span data-ttu-id="8adef-114">Vous créez cette grille de page à l’aide de l' **espace entre les formes** et les valeurs de **taille moyenne des formes** dans la boîte de dialogue **disposition et positionnement** .</span><span class="sxs-lookup"><span data-stu-id="8adef-114">You create this page grid by using the **Space between shapes** and the **Average shape size** values in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="8adef-115">(Sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , cliquez sur **disposition et positionnement**, puis cliquez sur **espacement**.)</span><span class="sxs-lookup"><span data-stu-id="8adef-115">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span> 
  
<span data-ttu-id="8adef-116">Lorsque vous activez cette fonction, l'application aligne le point central de chaque forme positionnable sur le centre d'un bloc de la grille de page interne.</span><span class="sxs-lookup"><span data-stu-id="8adef-116">When you enable this feature, the application aligns each placeable shape's center point with the center of a block on the internal page grid.</span></span> 
  
<span data-ttu-id="8adef-117">Pour obtenir une référence à la cellule EnableGrid par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="8adef-117">To get a reference to the EnableGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8adef-118">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8adef-118">Cell name:</span></span>  <br/> |<span data-ttu-id="8adef-119">EnableGrid</span><span class="sxs-lookup"><span data-stu-id="8adef-119">EnableGrid</span></span>  <br/> |
   
<span data-ttu-id="8adef-120">Pour obtenir une référence à la cellule EnableGrid par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8adef-120">To get a reference to the EnableGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8adef-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8adef-121">Section index:</span></span>  <br/> |<span data-ttu-id="8adef-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8adef-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8adef-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8adef-123">Row index:</span></span>  <br/> |<span data-ttu-id="8adef-124">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="8adef-124">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="8adef-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8adef-125">Cell index:</span></span>  <br/> |<span data-ttu-id="8adef-126">**visPLOEnableGrid**</span><span class="sxs-lookup"><span data-stu-id="8adef-126">**visPLOEnableGrid**</span></span> <br/> |
   

