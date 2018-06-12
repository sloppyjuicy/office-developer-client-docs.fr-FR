---
title: Active, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Détermine si le calque est actif. Les formes sans calque pré-attribué sont affectées aux calques actifs lorsque vous les faites glisser sur la page de dessin.
ms.openlocfilehash: 81d3ec083e207a927c46dda99e2b7f42c0a7bd8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788004"
---
# <a name="active-cell-layers-section"></a><span data-ttu-id="e80cc-104">Active, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="e80cc-104">Active Cell (Layers Section)</span></span>

<span data-ttu-id="e80cc-p102">Détermine si le calque est actif. Les formes sans calque pré-attribué sont affectées aux calques actifs lorsque vous les faites glisser sur la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="e80cc-p102">Specifies whether the layer is active. Shapes without pre-assigned layers are assigned to the active layer(s) when you drag them onto the drawing page.</span></span>
  
|<span data-ttu-id="e80cc-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e80cc-107">**Value**</span></span>|<span data-ttu-id="e80cc-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="e80cc-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e80cc-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="e80cc-109">TRUE</span></span>  <br/> |<span data-ttu-id="e80cc-110">Le calque est actif.</span><span class="sxs-lookup"><span data-stu-id="e80cc-110">Layer is active.</span></span>  <br/> |
|<span data-ttu-id="e80cc-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="e80cc-111">FALSE</span></span>  <br/> |<span data-ttu-id="e80cc-112">Calque n’est pas actif.</span><span class="sxs-lookup"><span data-stu-id="e80cc-112">Layer is not active.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e80cc-113">Note</span><span class="sxs-lookup"><span data-stu-id="e80cc-113">Remarks</span></span>

<span data-ttu-id="e80cc-114">La valeur de cette cellule correspond au paramètre **actif** de la boîte de dialogue **Propriétés des calques** (dans le groupe **modification** , sous l’onglet **accueil** , cliquez sur **calques**, puis cliquez sur **Propriétés des calques**).</span><span class="sxs-lookup"><span data-stu-id="e80cc-114">The value in this cell corresponds to the **Active** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="e80cc-115">Pour obtenir une référence à la cellule Active par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="e80cc-115">To get a reference to the Active cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e80cc-116">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e80cc-116">Cell name:</span></span>  <br/> |<span data-ttu-id="e80cc-117">Layers.Active [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e80cc-117">Layers.Active[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e80cc-118">Pour obtenir une référence à la cellule Active par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e80cc-118">To get a reference to the Active cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e80cc-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e80cc-119">Section index:</span></span>  <br/> |<span data-ttu-id="e80cc-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="e80cc-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="e80cc-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e80cc-121">Row index:</span></span>  <br/> |<span data-ttu-id="e80cc-122">**visRowLayer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e80cc-122">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e80cc-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e80cc-123">Cell index:</span></span>  <br/> |<span data-ttu-id="e80cc-124">**visLayerActive**</span><span class="sxs-lookup"><span data-stu-id="e80cc-124">**visLayerActive**</span></span> <br/> |
   

