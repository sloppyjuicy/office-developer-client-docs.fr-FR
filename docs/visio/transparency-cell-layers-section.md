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
ms.openlocfilehash: 7c205612436e7731f268e17c851616beebf809dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789928"
---
# <a name="transparency-cell-layers-section"></a><span data-ttu-id="da0ee-103">Transparency, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="da0ee-103">Transparency Cell (Layers Section)</span></span>

<span data-ttu-id="da0ee-104">Définit le niveau de transparence de la couleur d'un calque.</span><span class="sxs-lookup"><span data-stu-id="da0ee-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="da0ee-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="da0ee-105">**Value**</span></span>|<span data-ttu-id="da0ee-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="da0ee-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="da0ee-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="da0ee-107">0 - 100</span></span>  <br/> |<span data-ttu-id="da0ee-p101">Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="da0ee-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da0ee-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="da0ee-110">Remarks</span></span>

<span data-ttu-id="da0ee-111">Les valeurs sont arrondies au pourcentage le plus proche.</span><span class="sxs-lookup"><span data-stu-id="da0ee-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="da0ee-112">Une valeur de 100 % est complètement transparente.</span><span class="sxs-lookup"><span data-stu-id="da0ee-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="da0ee-113">Bien qu’un calque dont la couleur transparente complètement la même page de dessin s’affiche en tant que couche qui n’a aucune couleur, il interagit avec d’autres objets dans la page de la même manière que si sa transparence ont été 0 %.</span><span class="sxs-lookup"><span data-stu-id="da0ee-113">Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span> <span data-ttu-id="da0ee-114">Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **accueil** , dans le groupe **modification** , cliquez sur **calques**, puis cliquez sur **Propriétés des calques**).</span><span class="sxs-lookup"><span data-stu-id="da0ee-114">You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="da0ee-115">Pour obtenir une référence à la cellule Transparency par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="da0ee-115">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da0ee-116">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="da0ee-116">Cell name:</span></span>  <br/> |<span data-ttu-id="da0ee-117">Layers.ColorTrans [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="da0ee-117">Layers.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="da0ee-118">Pour obtenir une référence à la cellule Transparency par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="da0ee-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da0ee-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="da0ee-119">Section index:</span></span>  <br/> |<span data-ttu-id="da0ee-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="da0ee-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="da0ee-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="da0ee-121">Row index:</span></span>  <br/> |<span data-ttu-id="da0ee-122">**visRowLayer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="da0ee-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="da0ee-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="da0ee-123">Cell index:</span></span>  <br/> |<span data-ttu-id="da0ee-124">**visLayerColorTrans**</span><span class="sxs-lookup"><span data-stu-id="da0ee-124">**visLayerColorTrans**</span></span> <br/> |
   

