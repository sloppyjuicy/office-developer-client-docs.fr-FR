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
ms.openlocfilehash: 9da5e06a7fbf6ae77a49fb0410aefb406e2afecb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422830"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a><span data-ttu-id="31338-104">ImgWidth, cellule (section Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="31338-104">ImgWidth Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="31338-p102">Détermine la largeur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="31338-p102">Determines the width of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="31338-107">= Largeur \* 1</span><span class="sxs-lookup"><span data-stu-id="31338-107">= Width \* 1</span></span>
  
<span data-ttu-id="31338-108">Toute découpe de l'objet modifie le facteur par lequel la largeur est multipliée.</span><span class="sxs-lookup"><span data-stu-id="31338-108">Cropping the object changes the factor by which Width is multiplied.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31338-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="31338-109">Remarks</span></span>

<span data-ttu-id="31338-110">Pour obtenir une référence à la cellule ImgWidth par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="31338-110">To get a reference to the ImgWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31338-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="31338-111">Cell name:</span></span>  <br/> | <span data-ttu-id="31338-112">ImgWidth</span><span class="sxs-lookup"><span data-stu-id="31338-112">ImgWidth</span></span>  <br/> |
   
<span data-ttu-id="31338-113">Pour obtenir une référence à la cellule ImgWidth à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="31338-113">To get a reference to the ImgWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31338-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="31338-114">Section index:</span></span>  <br/> |<span data-ttu-id="31338-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="31338-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="31338-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="31338-116">Row index:</span></span>  <br/> |<span data-ttu-id="31338-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="31338-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="31338-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="31338-118">Cell index:</span></span>  <br/> |<span data-ttu-id="31338-119">**visFrgnImgWidth**</span><span class="sxs-lookup"><span data-stu-id="31338-119">**visFrgnImgWidth**</span></span> <br/> |
   

