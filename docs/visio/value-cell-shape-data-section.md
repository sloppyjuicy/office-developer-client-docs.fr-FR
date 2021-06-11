---
title: Value, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Contient la valeur de l’élément de données de forme telle qu’elle est saisie dans la boîte de dialogue Définir les données de forme.
ms.openlocfilehash: 40d9e7fdd92ac8fa800a146ea45bbcd002ace87b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431903"
---
# <a name="value-cell-shape-data-section"></a><span data-ttu-id="b32ee-103">Value, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="b32ee-103">Value Cell (Shape Data Section)</span></span>

<span data-ttu-id="b32ee-104">Contient la valeur de l’élément de données de forme telle qu’elle est saisie dans la boîte de dialogue **Définir les données de forme**.</span><span class="sxs-lookup"><span data-stu-id="b32ee-104">Contains the shape data item's value as entered in the **Define Shape Data** dialog box.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b32ee-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="b32ee-105">Remarks</span></span>

<span data-ttu-id="b32ee-p101">Les formules entrées dans cette cellule sont remplacées par les valeurs entrées dans la boîte de dialogue **Définir les données de forme**. Cette règle est d’application même si vous utilisez la fonction GUARD pour protéger la formule.</span><span class="sxs-lookup"><span data-stu-id="b32ee-p101">Formulas entered in this cell are overridden by values entered in the **Define Shape Data** dialog box. This is true even if you use the GUARD function to protect the formula.</span></span> 
  
<span data-ttu-id="b32ee-108">Pour obtenir une référence à la cellule Value par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b32ee-108">To get a reference to the Value cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b32ee-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="b32ee-109">Cell name:</span></span>  <br/> | <span data-ttu-id="b32ee-110">Prop.  *Nom*  . Valeur où Prop.  *Le nom*  est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="b32ee-110">Prop.  *Name*  .Value where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="b32ee-111">Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b32ee-111">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b32ee-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b32ee-112">Section index:</span></span>  <br/> |<span data-ttu-id="b32ee-113">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="b32ee-113">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="b32ee-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b32ee-114">Row index:</span></span>  <br/> |<span data-ttu-id="b32ee-115">**visRowProp**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b32ee-115">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b32ee-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b32ee-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b32ee-117">**visCustPropsValue**</span><span class="sxs-lookup"><span data-stu-id="b32ee-117">**visCustPropsValue**</span></span> <br/> |
   

