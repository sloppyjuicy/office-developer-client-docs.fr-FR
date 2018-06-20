---
title: ClippingPath, cellule (Section Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contient une référence à la géométrie d’une image délimitée par le chemin d’accès.
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788254"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="7dfd4-103">ClippingPath, cellule (Section Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="7dfd4-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="7dfd4-104">Contient une référence à la géométrie d’une image délimitée par le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7dfd4-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="7dfd4-105">Remarks</span></span>

<span data-ttu-id="7dfd4-106">Si la cellule **ClippingPath** pointe vers un chemin d’accès valide, l’image est découpée afin que l’image s’affiche dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="7dfd4-107">Si la cellule **ClippingPath** est vide ou contient une entrée non valide, l’image est rendue par un élément rectangulaire, en utilisant les valeurs à l’échelle et de décalage.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7dfd4-108">Uniquement les chemins d’accès définis par une section [Geometry](geometry-section.md) dans la feuille ShapeSheet de l’image sont des entrées valides pour la cellule **ClippingPath** .</span><span class="sxs-lookup"><span data-stu-id="7dfd4-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="7dfd4-109">Références entre différentes feuilles ne peut pas être utilisés pour définir un masque d’image.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="7dfd4-110">Pour obtenir une référence à la cellule **ClippingPath** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="7dfd4-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7dfd4-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7dfd4-111">Cell name:</span></span>  <br/> | <span data-ttu-id="7dfd4-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="7dfd4-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="7dfd4-113">Pour obtenir une référence à la cellule **ClippingPath** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7dfd4-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7dfd4-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7dfd4-114">Section index:</span></span>  <br/> |<span data-ttu-id="7dfd4-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7dfd4-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7dfd4-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7dfd4-116">Row index:</span></span>  <br/> |<span data-ttu-id="7dfd4-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="7dfd4-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="7dfd4-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7dfd4-118">Cell index:</span></span>  <br/> |<span data-ttu-id="7dfd4-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="7dfd4-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="7dfd4-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="7dfd4-120">Example</span></span>

<span data-ttu-id="7dfd4-121">Vous pouvez modifier la forme de délimitation d’une image à un ovale en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="7dfd4-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="7dfd4-122">Insérez l’image sur la zone de dessin.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="7dfd4-123">Cliquez sur l’image, puis sélectionnez **Afficher la feuille ShapeSheet**.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="7dfd4-124">Avec le bouton droit n’importe où dans la feuille ShapeSheet et sélectionnez **Insérer une Section**.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="7dfd4-125">Dans la boîte de dialogue **Insérer une Section** , sélectionnez la **géométrie** , puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="7dfd4-126">Dans la section Geometry nouveaux (par exemple, « Geometry2 »), supprimez tout sauf une ligne.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="7dfd4-127">Avec le bouton droit de la ligne restante, puis sur **Modifier le Type de ligne**.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="7dfd4-128">Dans la boîte de dialogue **Modifier le Type de ligne** , sélectionnez **Ellipse** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="7dfd4-129">Dans la section **Foreign Image** , définir la formule pour la cellule **ClippingPath** à `="Geometry2.Path"` , puis acceptez la formule.</span><span class="sxs-lookup"><span data-stu-id="7dfd4-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

