---
title: ClippingPath Cell (Foreign Image Info Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contient une référence à la géométrie du chemin d’accès d’une image.
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425511"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="47d23-103">ClippingPath Cell (Foreign Image Info Section)</span><span class="sxs-lookup"><span data-stu-id="47d23-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="47d23-104">Contient une référence à la géométrie du chemin d’accès d’une image.</span><span class="sxs-lookup"><span data-stu-id="47d23-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="47d23-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="47d23-105">Remarks</span></span>

<span data-ttu-id="47d23-106">Si la **cellule ClippingPath** pointe vers un chemin d’accès valide, l’image est découpée de sorte que l’image soit restituer à l’intérieur du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="47d23-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="47d23-107">Si la **cellule ClippingPath** est vide ou contient une entrée non valide, l’image est rendue avec un clip rectangulaire, à l’aide des valeurs d’échelle et de décalage.</span><span class="sxs-lookup"><span data-stu-id="47d23-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="47d23-108">Seuls les chemins définis par une section [Geometry](geometry-section.md) dans la feuille ShapeSheet de l’image sont des entrées valides pour **la cellule ClippingPath.**</span><span class="sxs-lookup"><span data-stu-id="47d23-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="47d23-109">Les références de feuille croisée ne peuvent pas être utilisées pour définir un chemin de découpage d’image.</span><span class="sxs-lookup"><span data-stu-id="47d23-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="47d23-110">Pour obtenir une référence à la cellule **ClippingPath** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="47d23-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="47d23-111">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="47d23-111">Cell name:</span></span>  <br/> | <span data-ttu-id="47d23-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="47d23-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="47d23-113">Pour obtenir une référence à la cellule **ClippingPath** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="47d23-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="47d23-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="47d23-114">Section index:</span></span>  <br/> |<span data-ttu-id="47d23-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="47d23-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="47d23-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="47d23-116">Row index:</span></span>  <br/> |<span data-ttu-id="47d23-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="47d23-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="47d23-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="47d23-118">Cell index:</span></span>  <br/> |<span data-ttu-id="47d23-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="47d23-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="47d23-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="47d23-120">Example</span></span>

<span data-ttu-id="47d23-121">Vous pouvez modifier la forme de bounding d’une image en ovale en faisant ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="47d23-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="47d23-122">Insérez l’image sur la zone de dessin.</span><span class="sxs-lookup"><span data-stu-id="47d23-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="47d23-123">Cliquez avec le bouton droit sur l’image, puis **sélectionnez Afficher la feuille ShapeSheet.**</span><span class="sxs-lookup"><span data-stu-id="47d23-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="47d23-124">Cliquez avec le bouton droit n’importe où dans la feuille ShapeSheet et **sélectionnez Insérer une section.**</span><span class="sxs-lookup"><span data-stu-id="47d23-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="47d23-125">Dans la boîte de dialogue Insérer une **section,** **sélectionnez Geometry,** puis cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="47d23-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="47d23-126">Dans la nouvelle section Geometry (par exemple, « Geometry2 »), supprimez toutes les lignes sauf une.</span><span class="sxs-lookup"><span data-stu-id="47d23-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="47d23-127">Cliquez avec le bouton droit sur la ligne restante, puis cliquez **sur Modifier le type de ligne.**</span><span class="sxs-lookup"><span data-stu-id="47d23-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="47d23-128">Dans la **boîte de dialogue Modifier le type de** ligne, sélectionnez **Ellipse,** puis cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="47d23-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="47d23-129">Dans la section **Image étrangère,** définissez la formule de la cellule **ClippingPath**  `="Geometry2.Path"` sur, puis acceptez la formule.</span><span class="sxs-lookup"><span data-stu-id="47d23-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

