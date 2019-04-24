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
ms.openlocfilehash: 4266debc318c839bdd29fa818d11b5e1da669a9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357812"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="9133b-103">Visible, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="9133b-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="9133b-104">Indique si les formes appartenant au calque sont visibles sur la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="9133b-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="9133b-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="9133b-105">**Value**</span></span>|<span data-ttu-id="9133b-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="9133b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9133b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9133b-107">TRUE</span></span>  <br/> |<span data-ttu-id="9133b-108">Les formes sont visibles.</span><span class="sxs-lookup"><span data-stu-id="9133b-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="9133b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9133b-109">FALSE</span></span>  <br/> |<span data-ttu-id="9133b-110">Les formes sont masquées.</span><span class="sxs-lookup"><span data-stu-id="9133b-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9133b-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="9133b-111">Remarks</span></span>

<span data-ttu-id="9133b-112">Cette cellule correspond à l' **option visible** dans la boîte de dialogue **Propriétés** des calques (sous l'onglet **Accueil** , dans le groupe **modification** , cliquez sur calques, puis sur **Propriétés des calques** ). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9133b-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="9133b-113">Pour obtenir une référence à la cellule Visible par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9133b-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9133b-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="9133b-114">Cell name:</span></span>  <br/> |<span data-ttu-id="9133b-115">Layers. visible [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9133b-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9133b-116">Pour obtenir une référence à la cellule Visible par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9133b-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9133b-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9133b-117">Section index:</span></span>  <br/> |<span data-ttu-id="9133b-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="9133b-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="9133b-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9133b-119">Row index:</span></span>  <br/> |<span data-ttu-id="9133b-120">**visRowLayer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9133b-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9133b-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9133b-121">Cell index:</span></span>  <br/> |<span data-ttu-id="9133b-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="9133b-122">**visLayerVisible**</span></span> <br/> |
   

