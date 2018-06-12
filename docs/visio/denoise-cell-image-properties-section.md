---
title: Denoise, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: Supprime le bruit (pixels comportant des niveaux de couleur répartis de façon aléatoire) d'une image en mode point. La valeur par défaut est 0 %.
ms.openlocfilehash: f08d09126a24935c0dd4dcda5e88fdd559c8d176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788474"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="b844c-104">Denoise, cellule (section Image Properties)</span><span class="sxs-lookup"><span data-stu-id="b844c-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="b844c-p102">Supprime le bruit (pixels comportant des niveaux de couleur répartis de façon aléatoire) d'une image en mode point. La valeur par défaut est 0 %.</span><span class="sxs-lookup"><span data-stu-id="b844c-p102">Removes noise (pixels with randomly distributed color levels) from a bitmap image. The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b844c-107">Note</span><span class="sxs-lookup"><span data-stu-id="b844c-107">Remarks</span></span>

<span data-ttu-id="b844c-108">Pour obtenir une référence à la cellule Denoise par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="b844c-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b844c-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b844c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="b844c-110">Denoise</span><span class="sxs-lookup"><span data-stu-id="b844c-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="b844c-111">Pour obtenir une référence à la cellule Denoise par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b844c-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b844c-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b844c-112">Section index:</span></span>  <br/> |<span data-ttu-id="b844c-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b844c-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b844c-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b844c-114">Row index:</span></span>  <br/> |<span data-ttu-id="b844c-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="b844c-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="b844c-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b844c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b844c-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="b844c-117">**visImageDenoise**</span></span> <br/> |
   

