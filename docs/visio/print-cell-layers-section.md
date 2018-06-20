---
title: Print, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Indique si les formes appartenant au calque peuvent être imprimées.
ms.openlocfilehash: cd5b2830ba8bd20cb435cdc2bca4bd55fd5a5438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789352"
---
# <a name="print-cell-layers-section"></a><span data-ttu-id="291ba-103">Print, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="291ba-103">Print Cell (Layers Section)</span></span>

<span data-ttu-id="291ba-104">Indique si les formes appartenant au calque peuvent être imprimées.</span><span class="sxs-lookup"><span data-stu-id="291ba-104">Specifies whether shapes belonging to the layer can be printed.</span></span>
  
|<span data-ttu-id="291ba-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="291ba-105">**Value**</span></span>|<span data-ttu-id="291ba-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="291ba-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="291ba-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="291ba-107">TRUE</span></span>  <br/> |<span data-ttu-id="291ba-108">Les formes peuvent être imprimées.</span><span class="sxs-lookup"><span data-stu-id="291ba-108">Shapes can be printed.</span></span>  <br/> |
|<span data-ttu-id="291ba-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="291ba-109">FALSE</span></span>  <br/> |<span data-ttu-id="291ba-110">Les formes ne peuvent pas être imprimées.</span><span class="sxs-lookup"><span data-stu-id="291ba-110">Shapes cannot be printed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="291ba-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="291ba-111">Remarks</span></span>

<span data-ttu-id="291ba-112">Vous pouvez également définir cette valeur à l’aide de l’option **Imprimer** dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **accueil** , dans le groupe **modification** , cliquez sur **calques**, puis cliquez sur **Propriétés des calques**).</span><span class="sxs-lookup"><span data-stu-id="291ba-112">You can also set this value by using the **Print** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="291ba-113">Pour obtenir une référence à la cellule Print par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="291ba-113">To get a reference to the Print cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="291ba-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="291ba-114">Cell name:</span></span>  <br/> |<span data-ttu-id="291ba-115">Layers.Print [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="291ba-115">Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="291ba-116">Pour obtenir une référence à la cellule Print par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="291ba-116">To get a reference to the Print cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="291ba-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="291ba-117">Section index:</span></span>  <br/> |<span data-ttu-id="291ba-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="291ba-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="291ba-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="291ba-119">Row index:</span></span>  <br/> |<span data-ttu-id="291ba-120">**visRowLayer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="291ba-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="291ba-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="291ba-121">Cell index:</span></span>  <br/> |<span data-ttu-id="291ba-122">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="291ba-122">**visDocPreviewScope**</span></span> <br/> |
   

