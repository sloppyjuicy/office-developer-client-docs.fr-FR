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
ms.openlocfilehash: f97f7dc09d1f882452ae2234882de45f06bd0da1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417433"
---
# <a name="active-cell-layers-section"></a><span data-ttu-id="56c32-104">Active, cellule (section Layers)</span><span class="sxs-lookup"><span data-stu-id="56c32-104">Active Cell (Layers Section)</span></span>

<span data-ttu-id="56c32-p102">Détermine si le calque est actif. Les formes sans calque pré-attribué sont affectées aux calques actifs lorsque vous les faites glisser sur la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="56c32-p102">Specifies whether the layer is active. Shapes without pre-assigned layers are assigned to the active layer(s) when you drag them onto the drawing page.</span></span>
  
|<span data-ttu-id="56c32-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="56c32-107">**Value**</span></span>|<span data-ttu-id="56c32-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="56c32-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56c32-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="56c32-109">TRUE</span></span>  <br/> |<span data-ttu-id="56c32-110">Le calque est actif.</span><span class="sxs-lookup"><span data-stu-id="56c32-110">Layer is active.</span></span>  <br/> |
|<span data-ttu-id="56c32-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="56c32-111">FALSE</span></span>  <br/> |<span data-ttu-id="56c32-112">Le calque n'est pas actif.</span><span class="sxs-lookup"><span data-stu-id="56c32-112">Layer is not active.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56c32-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="56c32-113">Remarks</span></span>

<span data-ttu-id="56c32-114">La valeur de cette cellule correspond au paramètre **Actif** de la boîte de dialogue **Propriétés des calques** (dans le groupe **Modification** de l’onglet **Accueil**, cliquez sur **Calques**, puis sur **Propriétés du calque**).</span><span class="sxs-lookup"><span data-stu-id="56c32-114">The value in this cell corresponds to the **Active** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="56c32-115">Pour obtenir une référence à la cellule Active par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="56c32-115">To get a reference to the Active cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56c32-116">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="56c32-116">Cell name:</span></span>  <br/> |<span data-ttu-id="56c32-117">Layers.Active[ *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="56c32-117">Layers.Active[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="56c32-118">Pour obtenir une référence à la cellule Active à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="56c32-118">To get a reference to the Active cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56c32-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="56c32-119">Section index:</span></span>  <br/> |<span data-ttu-id="56c32-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="56c32-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="56c32-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="56c32-121">Row index:</span></span>  <br/> |<span data-ttu-id="56c32-122">**visRowLayer**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="56c32-122">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="56c32-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="56c32-123">Cell index:</span></span>  <br/> |<span data-ttu-id="56c32-124">**visLayerActive**</span><span class="sxs-lookup"><span data-stu-id="56c32-124">**visLayerActive**</span></span> <br/> |
   

