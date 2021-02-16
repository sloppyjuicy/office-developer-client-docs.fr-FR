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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405316"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="3abea-103">Invisible, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="3abea-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="3abea-104">Détermine si l’élément de données de forme est visible ou non dans la fenêtre **Données de forme**.</span><span class="sxs-lookup"><span data-stu-id="3abea-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="3abea-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3abea-105">**Value**</span></span>|<span data-ttu-id="3abea-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="3abea-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3abea-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3abea-107">TRUE</span></span>  <br/> | <span data-ttu-id="3abea-108">Les données de forme ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="3abea-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="3abea-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3abea-109">FALSE</span></span>  <br/> | <span data-ttu-id="3abea-110">L'élément de données de forme est visible.</span><span class="sxs-lookup"><span data-stu-id="3abea-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3abea-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="3abea-111">Remarks</span></span>

<span data-ttu-id="3abea-112">La valeur de cette cellule correspond à la case à cocher **Masquer** dans la boîte de dialogue **Définir les données de forme** (cliquez avec le bouton droit sur la forme, pointez sur **Données**, puis cliquez sur **Définir les données de forme**).</span><span class="sxs-lookup"><span data-stu-id="3abea-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="3abea-113">Pour obtenir une référence à la cellule Invisible par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="3abea-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3abea-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="3abea-114">Cell name:</span></span>  <br/> | <span data-ttu-id="3abea-115">Prop.  *nom*  . Invisible où Prop.  *nom est*  le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="3abea-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="3abea-116">Pour obtenir une référence à la cellule Invisible à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3abea-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3abea-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="3abea-117">Section index:</span></span>  <br/> |<span data-ttu-id="3abea-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="3abea-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="3abea-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="3abea-119">Row index:</span></span>  <br/> |<span data-ttu-id="3abea-120">**visRowProp**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3abea-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3abea-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3abea-121">Cell index:</span></span>  <br/> |<span data-ttu-id="3abea-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="3abea-122">**visCustPropsInvis**</span></span> <br/> |
   

