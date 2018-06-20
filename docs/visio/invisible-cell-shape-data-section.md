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
description: Spécifie si l’élément de données de forme est visible dans la fenêtre données de forme.
ms.openlocfilehash: 2cd3fcad5db7b1752c55055354f1ec842bff4899
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788838"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="c2df6-103">Invisible, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="c2df6-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="c2df6-104">Spécifie si l’élément de données de forme est visible dans la fenêtre **Données de forme** .</span><span class="sxs-lookup"><span data-stu-id="c2df6-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="c2df6-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c2df6-105">**Value**</span></span>|<span data-ttu-id="c2df6-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="c2df6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c2df6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c2df6-107">TRUE</span></span>  <br/> | <span data-ttu-id="c2df6-108">Les données de forme ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="c2df6-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="c2df6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c2df6-109">FALSE</span></span>  <br/> | <span data-ttu-id="c2df6-110">L'élément de données de forme est visible.</span><span class="sxs-lookup"><span data-stu-id="c2df6-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2df6-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="c2df6-111">Remarks</span></span>

<span data-ttu-id="c2df6-112">La valeur de cette cellule correspond à la case à cocher **masqué** dans la boîte de dialogue **Définir les données de forme** (avec le bouton droit de la forme, pointez sur **données**, puis cliquez sur **Définir les données de forme**).</span><span class="sxs-lookup"><span data-stu-id="c2df6-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="c2df6-113">Pour obtenir une référence à la cellule Invisible par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c2df6-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2df6-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c2df6-114">Cell name:</span></span>  <br/> | <span data-ttu-id="c2df6-115">Propriétés.  *nom* . Where invisible de propriétés.  *Name* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="c2df6-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="c2df6-116">Pour obtenir une référence à la cellule Invisible par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c2df6-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2df6-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c2df6-117">Section index:</span></span>  <br/> |<span data-ttu-id="c2df6-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="c2df6-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="c2df6-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c2df6-119">Row index:</span></span>  <br/> |<span data-ttu-id="c2df6-120">**visRowProp** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c2df6-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c2df6-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c2df6-121">Cell index:</span></span>  <br/> |<span data-ttu-id="c2df6-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="c2df6-122">**visCustPropsInvis**</span></span> <br/> |
   

