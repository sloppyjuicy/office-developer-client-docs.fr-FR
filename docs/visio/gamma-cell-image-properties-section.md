---
title: Gamma, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm410
localization_priority: Normal
ms.assetid: 3dcaee26-391c-0494-4380-890ee825dc47
description: Ajuste ou corrige l'intensité d'une image pour un périphérique de sortie spécifique tel qu'un moniteur ou un scanneur. La valeur par défaut est 1 (pas de correction).
ms.openlocfilehash: d00eb11ff1feffacf0d758bb25cdd56281e91327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315203"
---
# <a name="gamma-cell-image-properties-section"></a><span data-ttu-id="e0544-104">Gamma, cellule (section Image Properties)</span><span class="sxs-lookup"><span data-stu-id="e0544-104">Gamma Cell (Image Properties Section)</span></span>

<span data-ttu-id="e0544-p102">Ajuste ou corrige l'intensité d'une image pour un périphérique de sortie spécifique tel qu'un moniteur ou un scanneur. La valeur par défaut est 1 (pas de correction).</span><span class="sxs-lookup"><span data-stu-id="e0544-p102">Adjusts or corrects the intensity of an image for a particular output device, such as a monitor or scanner. The default value is 1 (no correction).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0544-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0544-107">Remarks</span></span>

<span data-ttu-id="e0544-108">Pour obtenir une référence à la cellule Gamma par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="e0544-108">To get a reference to the Gamma cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e0544-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e0544-109">Cell name:</span></span>  <br/> | <span data-ttu-id="e0544-110">Gamma</span><span class="sxs-lookup"><span data-stu-id="e0544-110">Gamma</span></span>  <br/> |
   
<span data-ttu-id="e0544-111">Pour obtenir une référence à la cellule Gamma à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e0544-111">To get a reference to the Gamma cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e0544-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e0544-112">Section index:</span></span>  <br/> |<span data-ttu-id="e0544-113">**Définis**</span><span class="sxs-lookup"><span data-stu-id="e0544-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e0544-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e0544-114">Row index:</span></span>  <br/> |<span data-ttu-id="e0544-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="e0544-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="e0544-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e0544-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e0544-117">**visImageGamma**</span><span class="sxs-lookup"><span data-stu-id="e0544-117">**visImageGamma**</span></span> <br/> |
   

