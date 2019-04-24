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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355971"
---
# <a name="value-cell-shape-data-section"></a><span data-ttu-id="d405e-103">Value, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="d405e-103">Value Cell (Shape Data Section)</span></span>

<span data-ttu-id="d405e-104">Contient la valeur de l’élément de données de forme telle qu’elle est saisie dans la boîte de dialogue **Définir les données de forme**.</span><span class="sxs-lookup"><span data-stu-id="d405e-104">Contains the shape data item's value as entered in the **Define Shape Data** dialog box.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d405e-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d405e-105">Remarks</span></span>

<span data-ttu-id="d405e-p101">Les formules entrées dans cette cellule sont remplacées par les valeurs entrées dans la boîte de dialogue **Définir les données de forme**. Cette règle est d’application même si vous utilisez la fonction GUARD pour protéger la formule.</span><span class="sxs-lookup"><span data-stu-id="d405e-p101">Formulas entered in this cell are overridden by values entered in the **Define Shape Data** dialog box. This is true even if you use the GUARD function to protect the formula.</span></span> 
  
<span data-ttu-id="d405e-108">Pour obtenir une référence à la cellule Value par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d405e-108">To get a reference to the Value cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d405e-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="d405e-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d405e-110">Hélice.  *Nom* . Valeur où prop.  *Name* est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="d405e-110">Prop.  *Name*  .Value where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="d405e-111">Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d405e-111">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d405e-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d405e-112">Section index:</span></span>  <br/> |<span data-ttu-id="d405e-113">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="d405e-113">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="d405e-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d405e-114">Row index:</span></span>  <br/> |<span data-ttu-id="d405e-115">**visRowProp** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d405e-115">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d405e-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d405e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d405e-117">**visCustPropsValue**</span><span class="sxs-lookup"><span data-stu-id="d405e-117">**visCustPropsValue**</span></span> <br/> |
   

