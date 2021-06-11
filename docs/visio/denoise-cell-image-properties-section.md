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
ms.openlocfilehash: f970fde22e864239ea3f3f9bcb704e7f4692e9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415802"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="70f41-104">Denoise, cellule (section Image Properties)</span><span class="sxs-lookup"><span data-stu-id="70f41-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="70f41-p102">Supprime le bruit (pixels comportant des niveaux de couleur répartis de façon aléatoire) d'une image en mode point. La valeur par défaut est 0 %.</span><span class="sxs-lookup"><span data-stu-id="70f41-p102">Removes noise (pixels with randomly distributed color levels) from a bitmap image. The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70f41-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="70f41-107">Remarks</span></span>

<span data-ttu-id="70f41-108">Pour obtenir une référence à la cellule Denoise par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="70f41-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="70f41-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="70f41-109">Cell name:</span></span>  <br/> | <span data-ttu-id="70f41-110">Denoise</span><span class="sxs-lookup"><span data-stu-id="70f41-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="70f41-111">Pour obtenir une référence à la cellule Denoise à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="70f41-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="70f41-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="70f41-112">Section index:</span></span>  <br/> |<span data-ttu-id="70f41-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="70f41-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="70f41-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="70f41-114">Row index:</span></span>  <br/> |<span data-ttu-id="70f41-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="70f41-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="70f41-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="70f41-116">Cell index:</span></span>  <br/> |<span data-ttu-id="70f41-117">**visImageDenimageDenimage**</span><span class="sxs-lookup"><span data-stu-id="70f41-117">**visImageDenoise**</span></span> <br/> |
   

