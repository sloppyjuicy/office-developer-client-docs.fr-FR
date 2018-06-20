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
description: Contient la valeur de l’élément de données de forme entré dans la boîte de dialogue Définir les données de forme.
ms.openlocfilehash: 5b373149360167585fc5a143ce9458703e219045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790005"
---
# <a name="value-cell-shape-data-section"></a><span data-ttu-id="6415c-103">Value, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="6415c-103">Value Cell (Shape Data Section)</span></span>

<span data-ttu-id="6415c-104">Contient la valeur de l’élément de données de forme entré dans la boîte de dialogue **Définir les données de forme** .</span><span class="sxs-lookup"><span data-stu-id="6415c-104">Contains the shape data item's value as entered in the **Define Shape Data** dialog box.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6415c-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="6415c-105">Remarks</span></span>

<span data-ttu-id="6415c-106">Les formules entrées dans cette cellule sont remplacées par les valeurs entrées dans la boîte de dialogue **Définir les données de forme** .</span><span class="sxs-lookup"><span data-stu-id="6415c-106">Formulas entered in this cell are overridden by values entered in the **Define Shape Data** dialog box.</span></span> <span data-ttu-id="6415c-107">Cela est vrai même si vous utilisez la fonction GUARD pour protéger la formule.</span><span class="sxs-lookup"><span data-stu-id="6415c-107">This is true even if you use the GUARD function to protect the formula.</span></span> 
  
<span data-ttu-id="6415c-108">Pour obtenir une référence à la cellule Value par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="6415c-108">To get a reference to the Value cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6415c-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6415c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="6415c-110">Propriétés.  *Nom* . Valeur de propriétés où.  *Name* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="6415c-110">Prop.  *Name*  .Value where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6415c-111">Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="6415c-111">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6415c-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6415c-112">Section index:</span></span>  <br/> |<span data-ttu-id="6415c-113">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="6415c-113">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="6415c-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6415c-114">Row index:</span></span>  <br/> |<span data-ttu-id="6415c-115">**visRowProp** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6415c-115">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6415c-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6415c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="6415c-117">**visCustPropsValue**</span><span class="sxs-lookup"><span data-stu-id="6415c-117">**visCustPropsValue**</span></span> <br/> |
   

