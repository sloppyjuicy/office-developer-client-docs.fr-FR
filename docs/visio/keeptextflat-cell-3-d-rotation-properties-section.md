---
title: KeepTextFlat Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indique si le texte d’une forme ignore la rotation de la forme en 3D. Ne s’applique pas à la rotation 2D.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422039"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="8ee9d-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span><span class="sxs-lookup"><span data-stu-id="8ee9d-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="8ee9d-105">Indique si le texte d’une forme ignore la rotation de la forme en 3D.</span><span class="sxs-lookup"><span data-stu-id="8ee9d-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="8ee9d-106">Ne s’applique pas à la rotation 2D.</span><span class="sxs-lookup"><span data-stu-id="8ee9d-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="8ee9d-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8ee9d-107">**Value**</span></span>|<span data-ttu-id="8ee9d-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="8ee9d-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ee9d-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="8ee9d-109">TRUE</span></span>  <br/> |<span data-ttu-id="8ee9d-110">Le texte de la forme ne pivote pas avec la géométrie de la forme.</span><span class="sxs-lookup"><span data-stu-id="8ee9d-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="8ee9d-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="8ee9d-111">FALSE</span></span>  <br/> |<span data-ttu-id="8ee9d-112">Le texte de la forme est transformé pour pivoter avec la géométrie de la forme.</span><span class="sxs-lookup"><span data-stu-id="8ee9d-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ee9d-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="8ee9d-113">Remarks</span></span>

<span data-ttu-id="8ee9d-114">Pour obtenir une référence à la cellule **KeepTextFlat** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="8ee9d-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ee9d-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="8ee9d-115">Cell name:</span></span>  <br/> |<span data-ttu-id="8ee9d-116">KeepTextFlat</span><span class="sxs-lookup"><span data-stu-id="8ee9d-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="8ee9d-117">Pour obtenir une référence à la **cellule KeepTextFlat** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8ee9d-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ee9d-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8ee9d-118">Section index:</span></span>  <br/> |<span data-ttu-id="8ee9d-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8ee9d-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8ee9d-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8ee9d-120">Row index:</span></span>  <br/> |<span data-ttu-id="8ee9d-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="8ee9d-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="8ee9d-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8ee9d-122">Cell index:</span></span>  <br/> |<span data-ttu-id="8ee9d-123">**visKeepTextFlat**</span><span class="sxs-lookup"><span data-stu-id="8ee9d-123">**visKeepTextFlat**</span></span> <br/> |
   

