---
title: ImgWidth, cellule (section Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: "Détermine la largeur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :"
ms.openlocfilehash: 3aab65d27d426287060f7572dad15174acb93199
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788818"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a><span data-ttu-id="156ab-104">ImgWidth, cellule (section Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="156ab-104">ImgWidth Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="156ab-p102">Détermine la largeur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="156ab-p102">Determines the width of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="156ab-107">= Largeur \* 1</span><span class="sxs-lookup"><span data-stu-id="156ab-107">= Width \* 1</span></span>
  
<span data-ttu-id="156ab-108">Toute découpe de l'objet modifie le facteur par lequel la largeur est multipliée.</span><span class="sxs-lookup"><span data-stu-id="156ab-108">Cropping the object changes the factor by which Width is multiplied.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="156ab-109">Note</span><span class="sxs-lookup"><span data-stu-id="156ab-109">Remarks</span></span>

<span data-ttu-id="156ab-110">Pour obtenir une référence à la cellule ImgWidth par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="156ab-110">To get a reference to the ImgWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="156ab-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="156ab-111">Cell name:</span></span>  <br/> | <span data-ttu-id="156ab-112">ImgWidth</span><span class="sxs-lookup"><span data-stu-id="156ab-112">ImgWidth</span></span>  <br/> |
   
<span data-ttu-id="156ab-113">Pour obtenir une référence à la cellule ImgWidth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="156ab-113">To get a reference to the ImgWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="156ab-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="156ab-114">Section index:</span></span>  <br/> |<span data-ttu-id="156ab-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="156ab-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="156ab-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="156ab-116">Row index:</span></span>  <br/> |<span data-ttu-id="156ab-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="156ab-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="156ab-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="156ab-118">Cell index:</span></span>  <br/> |<span data-ttu-id="156ab-119">**visFrgnImgWidth**</span><span class="sxs-lookup"><span data-stu-id="156ab-119">**visFrgnImgWidth**</span></span> <br/> |
   

