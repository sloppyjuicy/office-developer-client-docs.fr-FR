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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332808"
---
# <a name="glue-cell-layers-section"></a><span data-ttu-id="85ff4-103">Glue, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="85ff4-103">Glue Cell (Layers Section)</span></span>

<span data-ttu-id="85ff4-104">Détermine si les formes du calque peuvent être collées.</span><span class="sxs-lookup"><span data-stu-id="85ff4-104">Specifies whether shapes belonging to the layer can be glued.</span></span>
  
|<span data-ttu-id="85ff4-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="85ff4-105">**Value**</span></span>|<span data-ttu-id="85ff4-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="85ff4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85ff4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="85ff4-107">TRUE</span></span>  <br/> |<span data-ttu-id="85ff4-108">Le collage est activé.</span><span class="sxs-lookup"><span data-stu-id="85ff4-108">Glue is enabled.</span></span>  <br/> |
|<span data-ttu-id="85ff4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="85ff4-109">FALSE</span></span>  <br/> |<span data-ttu-id="85ff4-110">Le collage est désactivé.</span><span class="sxs-lookup"><span data-stu-id="85ff4-110">Glue is disabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85ff4-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="85ff4-111">Remarks</span></span>

<span data-ttu-id="85ff4-112">Cette cellule correspond à l' **option collage** dans la boîte de dialogue **Propriétés** des calques (sous l'onglet **Accueil** , dans le groupe **modification** , cliquez sur calques, puis sur **Propriétés des calques** ). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="85ff4-112">This cell corresponds to the **Glue** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="85ff4-113">Pour obtenir une référence à la cellule Glue par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="85ff4-113">To get a reference to the Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85ff4-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="85ff4-114">Cell name:</span></span>  <br/> |<span data-ttu-id="85ff4-115">Layers. Glue [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="85ff4-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="85ff4-116">Pour obtenir une référence à la cellule Glue à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="85ff4-116">To get a reference to the Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85ff4-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="85ff4-117">Section index:</span></span>  <br/> |<span data-ttu-id="85ff4-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="85ff4-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="85ff4-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="85ff4-119">Row index:</span></span>  <br/> |<span data-ttu-id="85ff4-120">**visRowLayer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="85ff4-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="85ff4-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="85ff4-121">Cell index:</span></span>  <br/> |<span data-ttu-id="85ff4-122">**visLayerGlue**</span><span class="sxs-lookup"><span data-stu-id="85ff4-122">**visLayerGlue**</span></span> <br/> |
   

