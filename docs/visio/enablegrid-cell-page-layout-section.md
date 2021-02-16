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
description: Détermine si l’application aligne les formes sur une grille de page interne invisible lorsque vous configurez la disposition dans la boîte de dialogue Configurer la disposition. (Sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition.)
ms.openlocfilehash: 11299ca7c9b0ea050542baf97e2cab3a27fa52ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424440"
---
# <a name="enablegrid-cell-page-layout-section"></a><span data-ttu-id="1eeb2-104">EnableGrid, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="1eeb2-104">EnableGrid Cell (Page Layout Section)</span></span>

<span data-ttu-id="1eeb2-p102">Détermine si l’application aligne les formes sur une grille de page interne invisible lorsque vous configurez la disposition dans la boîte de dialogue **Configurer la disposition**. (Sous l’onglet **Création**, dans le groupe **Disposition**, cliquez sur **Nouvelle disposition de page**, puis cliquez sur **Autres options de disposition**.)</span><span class="sxs-lookup"><span data-stu-id="1eeb2-p102">Determines whether the application lays out shapes based on an internal, invisible page grid when you configure the layout in the **Configure Layout** dialog box. (On the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**.)</span></span>
  
|<span data-ttu-id="1eeb2-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="1eeb2-107">**Value**</span></span>|<span data-ttu-id="1eeb2-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="1eeb2-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1eeb2-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="1eeb2-109">TRUE</span></span>  <br/> |<span data-ttu-id="1eeb2-110">Utilise la grille de page interne.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-110">Use the internal page grid.</span></span>  <br/> |
|<span data-ttu-id="1eeb2-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="1eeb2-111">FALSE</span></span>  <br/> |<span data-ttu-id="1eeb2-112">N'utilise pas la grille de page interne.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-112">Do not use the internal page grid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1eeb2-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="1eeb2-113">Remarks</span></span>

<span data-ttu-id="1eeb2-p103">Vous créez cette grille de page au moyen des valeurs **Espace entre les formes** et **Taille de forme moyenne** dans la boîte de dialogue **Espacement : disposition et positionnement**. (Sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, cliquez sur **Disposition et positionnement**, puis cliquez sur **Espacement**.)</span><span class="sxs-lookup"><span data-stu-id="1eeb2-p103">You create this page grid by using the **Space between shapes** and the **Average shape size** values in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span> 
  
<span data-ttu-id="1eeb2-116">Lorsque vous activez cette fonction, l'application aligne le point central de chaque forme positionnable sur le centre d'un bloc de la grille de page interne.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-116">When you enable this feature, the application aligns each placeable shape's center point with the center of a block on the internal page grid.</span></span> 
  
<span data-ttu-id="1eeb2-117">Pour obtenir une référence à la cellule EnableGrid par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="1eeb2-117">To get a reference to the EnableGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1eeb2-118">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1eeb2-118">Cell name:</span></span>  <br/> |<span data-ttu-id="1eeb2-119">EnableGrid</span><span class="sxs-lookup"><span data-stu-id="1eeb2-119">EnableGrid</span></span>  <br/> |
   
<span data-ttu-id="1eeb2-120">Pour obtenir une référence à la cellule EnableGrid à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1eeb2-120">To get a reference to the EnableGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1eeb2-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1eeb2-121">Section index:</span></span>  <br/> |<span data-ttu-id="1eeb2-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1eeb2-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1eeb2-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1eeb2-123">Row index:</span></span>  <br/> |<span data-ttu-id="1eeb2-124">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="1eeb2-124">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="1eeb2-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1eeb2-125">Cell index:</span></span>  <br/> |<span data-ttu-id="1eeb2-126">**visPLOEnableGrid**</span><span class="sxs-lookup"><span data-stu-id="1eeb2-126">**visPLOEnableGrid**</span></span> <br/> |
   

