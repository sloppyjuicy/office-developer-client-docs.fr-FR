---
title: ImgHeight, cellule (section Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: "Détermine la hauteur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :"
ms.openlocfilehash: 983bb919dbfada65b6d9af464ecfa17c04e970c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788820"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="8c17a-104">ImgHeight, cellule (section Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="8c17a-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="8c17a-p102">Détermine la hauteur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="8c17a-p102">Determines the height of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="8c17a-107">= Hauteur \* 1</span><span class="sxs-lookup"><span data-stu-id="8c17a-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8c17a-108">Note</span><span class="sxs-lookup"><span data-stu-id="8c17a-108">Remarks</span></span>

<span data-ttu-id="8c17a-109">Pour obtenir une référence à la cellule ImgHeight par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="8c17a-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8c17a-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8c17a-110">Cell name:</span></span>  <br/> | <span data-ttu-id="8c17a-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="8c17a-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="8c17a-112">Pour obtenir une référence à la cellule ImgHeight par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8c17a-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8c17a-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8c17a-113">Section index:</span></span>  <br/> |<span data-ttu-id="8c17a-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8c17a-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8c17a-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8c17a-115">Row index:</span></span>  <br/> |<span data-ttu-id="8c17a-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="8c17a-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="8c17a-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8c17a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="8c17a-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="8c17a-118">**visFrgnImgHeight**</span></span> <br/> |
   

