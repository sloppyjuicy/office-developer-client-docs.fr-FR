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
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411196"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="d9377-104">ImgHeight, cellule (section Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="d9377-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="d9377-105">Détermine la hauteur de l'image de l'objet à l'intérieur de ses bordures.</span><span class="sxs-lookup"><span data-stu-id="d9377-105">Determines the height of the object's image within its border.</span></span> <span data-ttu-id="d9377-106">La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d9377-106">The default formula is:</span></span>
  
<span data-ttu-id="d9377-107">= Hauteur \* 1</span><span class="sxs-lookup"><span data-stu-id="d9377-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9377-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9377-108">Remarks</span></span>

<span data-ttu-id="d9377-109">Pour obtenir une référence à la cellule ImgHeight par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d9377-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d9377-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d9377-110">Cell name:</span></span>  <br/> | <span data-ttu-id="d9377-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="d9377-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="d9377-112">Pour obtenir une référence à la cellule ImgHeight à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d9377-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d9377-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d9377-113">Section index:</span></span>  <br/> |<span data-ttu-id="d9377-114">**Définis**</span><span class="sxs-lookup"><span data-stu-id="d9377-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d9377-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d9377-115">Row index:</span></span>  <br/> |<span data-ttu-id="d9377-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="d9377-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="d9377-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d9377-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d9377-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="d9377-118">**visFrgnImgHeight**</span></span> <br/> |
   

