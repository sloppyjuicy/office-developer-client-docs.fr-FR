---
title: Transparency, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: Définit le niveau de transparence de la couleur d'un calque.
ms.openlocfilehash: fe0aacf167b2400ca10e22a70c9086429f6059f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280951"
---
# <a name="transparency-cell-layers-section"></a><span data-ttu-id="77ee7-103">Transparency, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="77ee7-103">Transparency Cell (Layers Section)</span></span>

<span data-ttu-id="77ee7-104">Définit le niveau de transparence de la couleur d'un calque.</span><span class="sxs-lookup"><span data-stu-id="77ee7-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="77ee7-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="77ee7-105">**Value**</span></span>|<span data-ttu-id="77ee7-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="77ee7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77ee7-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="77ee7-107">0 - 100</span></span>  <br/> |<span data-ttu-id="77ee7-p101">Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="77ee7-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77ee7-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="77ee7-110">Remarks</span></span>

<span data-ttu-id="77ee7-p102">Les valeurs sont arrondies au demi-point le plus proche. Une valeur de 100 % correspond à une transparence totale. Même si un calque dont la couleur est entièrement transparente apparaît identique sur la page de dessin à un calque dépourvu de couleur, il interagit avec les autres objets de la page de la même façon que s’il avait une transparence de 0 %. Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **Accueil**, dans le groupe **Modification**, cliquez sur **Calques**, puis cliquez sur **Propriétés des calques**).</span><span class="sxs-lookup"><span data-stu-id="77ee7-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%. You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="77ee7-115">Pour obtenir une référence à la cellule Transparency par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="77ee7-115">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77ee7-116">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="77ee7-116">Cell name:</span></span>  <br/> |<span data-ttu-id="77ee7-117">Layers. ColorTrans [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="77ee7-117">Layers.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="77ee7-118">Pour obtenir une référence à la cellule Transparency par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="77ee7-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77ee7-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="77ee7-119">Section index:</span></span>  <br/> |<span data-ttu-id="77ee7-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="77ee7-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="77ee7-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="77ee7-121">Row index:</span></span>  <br/> |<span data-ttu-id="77ee7-122">**visRowLayer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="77ee7-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="77ee7-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="77ee7-123">Cell index:</span></span>  <br/> |<span data-ttu-id="77ee7-124">**visLayerColorTrans**</span><span class="sxs-lookup"><span data-stu-id="77ee7-124">**visLayerColorTrans**</span></span> <br/> |
   

