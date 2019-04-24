---
title: Invisible, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Détermine si l’élément de données de forme est visible ou non dans la fenêtre Données de forme.
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357266"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="b3a0a-103">Invisible, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="b3a0a-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="b3a0a-104">Détermine si l’élément de données de forme est visible ou non dans la fenêtre **Données de forme**.</span><span class="sxs-lookup"><span data-stu-id="b3a0a-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="b3a0a-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="b3a0a-105">**Value**</span></span>|<span data-ttu-id="b3a0a-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b3a0a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b3a0a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b3a0a-107">TRUE</span></span>  <br/> | <span data-ttu-id="b3a0a-108">Les données de forme ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="b3a0a-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="b3a0a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b3a0a-109">FALSE</span></span>  <br/> | <span data-ttu-id="b3a0a-110">L'élément de données de forme est visible.</span><span class="sxs-lookup"><span data-stu-id="b3a0a-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3a0a-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="b3a0a-111">Remarks</span></span>

<span data-ttu-id="b3a0a-112">La valeur de cette cellule correspond à la case à cocher **Masquer** dans la boîte de dialogue **Définir les données de forme** (cliquez avec le bouton droit sur la forme, pointez sur **Données**, puis cliquez sur **Définir les données de forme**).</span><span class="sxs-lookup"><span data-stu-id="b3a0a-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="b3a0a-113">Pour obtenir une référence à la cellule Invisible par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b3a0a-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3a0a-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="b3a0a-114">Cell name:</span></span>  <br/> | <span data-ttu-id="b3a0a-115">Hélice.  *nom* . Invisible où prop.  *Name* est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="b3a0a-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="b3a0a-116">Pour obtenir une référence à la cellule Invisible à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b3a0a-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3a0a-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b3a0a-117">Section index:</span></span>  <br/> |<span data-ttu-id="b3a0a-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="b3a0a-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="b3a0a-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b3a0a-119">Row index:</span></span>  <br/> |<span data-ttu-id="b3a0a-120">**visRowProp** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b3a0a-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b3a0a-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b3a0a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="b3a0a-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="b3a0a-122">**visCustPropsInvis**</span></span> <br/> |
   

