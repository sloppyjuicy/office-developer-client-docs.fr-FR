---
title: Glue, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Détermine si les formes du calque peuvent être collées.
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408515"
---
# <a name="glue-cell-layers-section"></a><span data-ttu-id="cf0c9-103">Glue, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="cf0c9-103">Glue Cell (Layers Section)</span></span>

<span data-ttu-id="cf0c9-104">Détermine si les formes du calque peuvent être collées.</span><span class="sxs-lookup"><span data-stu-id="cf0c9-104">Specifies whether shapes belonging to the layer can be glued.</span></span>
  
|<span data-ttu-id="cf0c9-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="cf0c9-105">**Value**</span></span>|<span data-ttu-id="cf0c9-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="cf0c9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf0c9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="cf0c9-107">TRUE</span></span>  <br/> |<span data-ttu-id="cf0c9-108">Le collage est activé.</span><span class="sxs-lookup"><span data-stu-id="cf0c9-108">Glue is enabled.</span></span>  <br/> |
|<span data-ttu-id="cf0c9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="cf0c9-109">FALSE</span></span>  <br/> |<span data-ttu-id="cf0c9-110">Le collage est désactivé.</span><span class="sxs-lookup"><span data-stu-id="cf0c9-110">Glue is disabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf0c9-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf0c9-111">Remarks</span></span>

<span data-ttu-id="cf0c9-112">Cette cellule correspond à l’option Coller dans la  boîte de  dialogue Propriétés des calques (sous l’onglet Accueil, dans le groupe Édition, cliquez sur Calques, puis sur Propriétés des **calques).**   </span><span class="sxs-lookup"><span data-stu-id="cf0c9-112">This cell corresponds to the **Glue** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="cf0c9-113">Pour obtenir une référence à la cellule Glue par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="cf0c9-113">To get a reference to the Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf0c9-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="cf0c9-114">Cell name:</span></span>  <br/> |<span data-ttu-id="cf0c9-115">Layers.Glue[  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="cf0c9-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="cf0c9-116">Pour obtenir une référence à la cellule Glue à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="cf0c9-116">To get a reference to the Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf0c9-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="cf0c9-117">Section index:</span></span>  <br/> |<span data-ttu-id="cf0c9-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="cf0c9-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="cf0c9-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="cf0c9-119">Row index:</span></span>  <br/> |<span data-ttu-id="cf0c9-120">**visRowLayer**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cf0c9-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="cf0c9-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="cf0c9-121">Cell index:</span></span>  <br/> |<span data-ttu-id="cf0c9-122">**visLayerGlue**</span><span class="sxs-lookup"><span data-stu-id="cf0c9-122">**visLayerGlue**</span></span> <br/> |
   

