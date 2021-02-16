---
title: SortKey, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Produit une chaîne qui détermine l’ordre dans lequel les éléments de la fenêtre Données de forme sont présentés.
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417853"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="35399-103">SortKey, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="35399-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="35399-104">Produit une chaîne qui détermine l’ordre dans lequel les éléments de la fenêtre **Données de forme** sont présentés.</span><span class="sxs-lookup"><span data-stu-id="35399-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="35399-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="35399-105">Remarks</span></span>

<span data-ttu-id="35399-106">Le calcul utilisé pour comparer les valeurs SortKey est basé sur les paramètres régionaux spécifiques et ne tient pas compte des majuscules et des minuscules.</span><span class="sxs-lookup"><span data-stu-id="35399-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="35399-107">Si les valeurs SortKey sont égales, les données de forme sont présentées dans l'ordre des lignes.</span><span class="sxs-lookup"><span data-stu-id="35399-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="35399-108">Les données de forme sans clé de tri sont répertoriées après les données de forme qui contiennent une clé de tri.</span><span class="sxs-lookup"><span data-stu-id="35399-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="35399-109">Entrez par exemple les clés de tri suivantes pour afficher les données de forme dans la fenêtre **Données de forme** dans l’ordre Référence article, Quantité, Prix.</span><span class="sxs-lookup"><span data-stu-id="35399-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="35399-110">*Row, Label et*  *SortKey*  font référence aux cellules de la ligne de données de forme.</span><span class="sxs-lookup"><span data-stu-id="35399-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="35399-111">Dans ce cas, les lignes de données de forme ont été nommées.</span><span class="sxs-lookup"><span data-stu-id="35399-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="35399-112">**Ligne**</span><span class="sxs-lookup"><span data-stu-id="35399-112">**Row**</span></span>|<span data-ttu-id="35399-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="35399-113">**Label**</span></span>|<span data-ttu-id="35399-114">**SortKey**</span><span class="sxs-lookup"><span data-stu-id="35399-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="35399-115">Prop.Item</span><span class="sxs-lookup"><span data-stu-id="35399-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="35399-116">Référence article</span><span class="sxs-lookup"><span data-stu-id="35399-116">Item Number</span></span>  <br/> | <span data-ttu-id="35399-117">1 </span><span class="sxs-lookup"><span data-stu-id="35399-117">1</span></span>  <br/> |
| <span data-ttu-id="35399-118">Prop.Price</span><span class="sxs-lookup"><span data-stu-id="35399-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="35399-119">Price</span><span class="sxs-lookup"><span data-stu-id="35399-119">Price</span></span>  <br/> | <span data-ttu-id="35399-120">3 </span><span class="sxs-lookup"><span data-stu-id="35399-120">3</span></span>  <br/> |
| <span data-ttu-id="35399-121">Prop.Quan</span><span class="sxs-lookup"><span data-stu-id="35399-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="35399-122">Quantité</span><span class="sxs-lookup"><span data-stu-id="35399-122">Quantity</span></span>  <br/> | <span data-ttu-id="35399-123">2 </span><span class="sxs-lookup"><span data-stu-id="35399-123">2</span></span>  <br/> |
   
<span data-ttu-id="35399-124">Pour obtenir une référence à la cellule SortKey par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="35399-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35399-125">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="35399-125">Cell name:</span></span>  <br/> | <span data-ttu-id="35399-126">Prop.  *Nom*  . SortKey où Prop.  *Name*  est le nom de la ligne de propriété personnalisée</span><span class="sxs-lookup"><span data-stu-id="35399-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="35399-127">Pour obtenir une référence à la cellule SortKey par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="35399-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35399-128">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="35399-128">Section index:</span></span>  <br/> |<span data-ttu-id="35399-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="35399-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="35399-130">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="35399-130">Row index:</span></span>  <br/> |<span data-ttu-id="35399-131">**visRowProp**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="35399-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="35399-132">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="35399-132">Cell index:</span></span>  <br/> |<span data-ttu-id="35399-133">**visCustPropsSortKey**</span><span class="sxs-lookup"><span data-stu-id="35399-133">**visCustPropsSortKey**</span></span> <br/> |
   

