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
description: Correspond à une chaîne qui détermine l’ordre dans lequel les éléments dans la fenêtre données de forme sont répertoriés.
ms.openlocfilehash: 1dbc093f2cee509531b8148563fbdb1a777a349f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789797"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="3bddb-103">SortKey, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="3bddb-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="3bddb-104">Correspond à une chaîne qui détermine l’ordre dans lequel les éléments dans la fenêtre **Données de forme** sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="3bddb-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3bddb-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="3bddb-105">Remarks</span></span>

<span data-ttu-id="3bddb-106">Le calcul utilisé pour comparer les valeurs SortKey est spécifiques aux paramètres régionaux et de la casse.</span><span class="sxs-lookup"><span data-stu-id="3bddb-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="3bddb-107">Si les valeurs SortKey sont égales, les données de forme sont répertoriées dans l’ordre des lignes.</span><span class="sxs-lookup"><span data-stu-id="3bddb-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="3bddb-108">Données de forme qui n’ont aucune clé tri sont répertoriées après les données de forme qui contiennent une clé de tri.</span><span class="sxs-lookup"><span data-stu-id="3bddb-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="3bddb-109">Voici un exemple d’utilisation des clés de tri pour afficher les données de forme dans la fenêtre **Données de forme** dans l’ordre : numéro d’article, quantité, prix.</span><span class="sxs-lookup"><span data-stu-id="3bddb-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="3bddb-110">*Ligne, intitulé* et *SortKey* faire référence à des cellules dans la ligne de données de forme.</span><span class="sxs-lookup"><span data-stu-id="3bddb-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="3bddb-111">Dans ce cas, les lignes de données de forme ont été nommés.</span><span class="sxs-lookup"><span data-stu-id="3bddb-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="3bddb-112">**Row**</span><span class="sxs-lookup"><span data-stu-id="3bddb-112">**Row**</span></span>|<span data-ttu-id="3bddb-113">**Étiquette**</span><span class="sxs-lookup"><span data-stu-id="3bddb-113">**Label**</span></span>|<span data-ttu-id="3bddb-114">**SortKey**</span><span class="sxs-lookup"><span data-stu-id="3bddb-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3bddb-115">Prop.Item</span><span class="sxs-lookup"><span data-stu-id="3bddb-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="3bddb-116">Référence article</span><span class="sxs-lookup"><span data-stu-id="3bddb-116">Item Number</span></span>  <br/> | <span data-ttu-id="3bddb-117">1</span><span class="sxs-lookup"><span data-stu-id="3bddb-117">1</span></span>  <br/> |
| <span data-ttu-id="3bddb-118">Prop.prix</span><span class="sxs-lookup"><span data-stu-id="3bddb-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="3bddb-119">Prix</span><span class="sxs-lookup"><span data-stu-id="3bddb-119">Price</span></span>  <br/> | <span data-ttu-id="3bddb-120">3</span><span class="sxs-lookup"><span data-stu-id="3bddb-120">3</span></span>  <br/> |
| <span data-ttu-id="3bddb-121">Prop.Quan</span><span class="sxs-lookup"><span data-stu-id="3bddb-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="3bddb-122">Quantité</span><span class="sxs-lookup"><span data-stu-id="3bddb-122">Quantity</span></span>  <br/> | <span data-ttu-id="3bddb-123">2</span><span class="sxs-lookup"><span data-stu-id="3bddb-123">2</span></span>  <br/> |
   
<span data-ttu-id="3bddb-124">Pour obtenir une référence à la cellule SortKey par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="3bddb-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3bddb-125">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3bddb-125">Cell name:</span></span>  <br/> | <span data-ttu-id="3bddb-126">Propriétés.  *Nom* . SortKey où de propriétés.  *Nom* est le nom de la ligne de propriété personnalisée</span><span class="sxs-lookup"><span data-stu-id="3bddb-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="3bddb-127">Pour obtenir une référence à la cellule SortKey par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3bddb-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3bddb-128">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="3bddb-128">Section index:</span></span>  <br/> |<span data-ttu-id="3bddb-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="3bddb-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="3bddb-130">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="3bddb-130">Row index:</span></span>  <br/> |<span data-ttu-id="3bddb-131">**visRowProp** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3bddb-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3bddb-132">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3bddb-132">Cell index:</span></span>  <br/> |<span data-ttu-id="3bddb-133">**visCustPropsSortKey**</span><span class="sxs-lookup"><span data-stu-id="3bddb-133">**visCustPropsSortKey**</span></span> <br/> |
   

