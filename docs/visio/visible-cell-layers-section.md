---
title: Visible, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Indique si les formes appartenant au calque sont visibles sur la page de dessin.
ms.openlocfilehash: 9a025403b1f5b46d2f439805a15954eaeeab2686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790009"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="f984f-103">Visible, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="f984f-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="f984f-104">Indique si les formes appartenant au calque sont visibles sur la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="f984f-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="f984f-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f984f-105">**Value**</span></span>|<span data-ttu-id="f984f-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="f984f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f984f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f984f-107">TRUE</span></span>  <br/> |<span data-ttu-id="f984f-108">Les formes sont visibles.</span><span class="sxs-lookup"><span data-stu-id="f984f-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="f984f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f984f-109">FALSE</span></span>  <br/> |<span data-ttu-id="f984f-110">Les formes sont masquées.</span><span class="sxs-lookup"><span data-stu-id="f984f-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f984f-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="f984f-111">Remarks</span></span>

<span data-ttu-id="f984f-112">Cette cellule correspond à l’option **Visible** dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **accueil** , dans le groupe **modification** , cliquez sur **calques**, puis cliquez sur **Propriétés des calques** ).</span><span class="sxs-lookup"><span data-stu-id="f984f-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="f984f-113">Pour obtenir une référence à la cellule Visible par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="f984f-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f984f-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f984f-114">Cell name:</span></span>  <br/> |<span data-ttu-id="f984f-115">Layers.Visible [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f984f-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f984f-116">Pour obtenir une référence à la cellule Visible par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f984f-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f984f-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f984f-117">Section index:</span></span>  <br/> |<span data-ttu-id="f984f-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="f984f-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="f984f-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f984f-119">Row index:</span></span>  <br/> |<span data-ttu-id="f984f-120">**visRowLayer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f984f-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f984f-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f984f-121">Cell index:</span></span>  <br/> |<span data-ttu-id="f984f-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="f984f-122">**visLayerVisible**</span></span> <br/> |
   

