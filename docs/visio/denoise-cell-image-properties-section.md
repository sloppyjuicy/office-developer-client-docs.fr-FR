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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360248"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="e58e7-104">Denoise, cellule (section Image Properties)</span><span class="sxs-lookup"><span data-stu-id="e58e7-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="e58e7-105">Supprime le bruit (pixels comportant des niveaux de couleur répartis de façon aléatoire) d'une image en mode point.</span><span class="sxs-lookup"><span data-stu-id="e58e7-105">Removes noise (pixels with randomly distributed color levels) from a bitmap image.</span></span> <span data-ttu-id="e58e7-106">La valeur par défaut est 0 %.</span><span class="sxs-lookup"><span data-stu-id="e58e7-106">The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e58e7-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="e58e7-107">Remarks</span></span>

<span data-ttu-id="e58e7-108">Pour obtenir une référence à la cellule Denoise par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="e58e7-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e58e7-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e58e7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="e58e7-110">Noise</span><span class="sxs-lookup"><span data-stu-id="e58e7-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="e58e7-111">Pour obtenir une référence à la cellule Denoise à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e58e7-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e58e7-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e58e7-112">Section index:</span></span>  <br/> |<span data-ttu-id="e58e7-113">**Définis**</span><span class="sxs-lookup"><span data-stu-id="e58e7-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e58e7-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e58e7-114">Row index:</span></span>  <br/> |<span data-ttu-id="e58e7-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="e58e7-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="e58e7-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e58e7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e58e7-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="e58e7-117">**visImageDenoise**</span></span> <br/> |
   

