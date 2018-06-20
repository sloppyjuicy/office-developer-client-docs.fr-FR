---
title: KeepTextFlat, cellule (Section Propriétés de Rotation 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indique si le texte d’une forme ignorera rotation d’une forme en 3D. Ne s’applique pas à la rotation 2D.
ms.openlocfilehash: cf8b964360e602b81a2a7b7ca79961921eeeb8b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788890"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a><span data-ttu-id="c0fb3-104">KeepTextFlat, cellule (Section Propriétés de Rotation 3D)</span><span class="sxs-lookup"><span data-stu-id="c0fb3-104">KeepTextFlat Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="c0fb3-105">Indique si le texte d’une forme ignorera rotation d’une forme en 3D.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-105">Indicates whether a shape's text will ignore the shape's rotation in 3-D.</span></span> <span data-ttu-id="c0fb3-106">Ne s’applique pas à la rotation 2D.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-106">Does not apply to 2-D rotation.</span></span> 
  
****

|<span data-ttu-id="c0fb3-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c0fb3-107">**Value**</span></span>|<span data-ttu-id="c0fb3-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0fb3-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0fb3-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="c0fb3-109">TRUE</span></span>  <br/> |<span data-ttu-id="c0fb3-110">Texte de la forme ne pivote pas avec la géométrie d’une forme.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-110">Shape text does not rotate with the shape's geometry.</span></span>  <br/> |
|<span data-ttu-id="c0fb3-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="c0fb3-111">FALSE</span></span>  <br/> |<span data-ttu-id="c0fb3-112">Texte de la forme est transformé pivote avec la géométrie d’une forme.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-112">Shape text is transformed to rotate with the shape's geometry.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0fb3-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0fb3-113">Remarks</span></span>

<span data-ttu-id="c0fb3-114">Pour obtenir une référence à la cellule **KeepTextFlat** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c0fb3-114">To get a reference to the **KeepTextFlat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0fb3-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c0fb3-115">Cell name:</span></span>  <br/> |<span data-ttu-id="c0fb3-116">KeepTextFlat</span><span class="sxs-lookup"><span data-stu-id="c0fb3-116">KeepTextFlat</span></span>  <br/> |
   
<span data-ttu-id="c0fb3-117">Pour obtenir une référence à la cellule **KeepTextFlat** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c0fb3-117">To get a reference to the **KeepTextFlat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0fb3-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c0fb3-118">Section index:</span></span>  <br/> |<span data-ttu-id="c0fb3-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0fb3-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c0fb3-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c0fb3-120">Row index:</span></span>  <br/> |<span data-ttu-id="c0fb3-121">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="c0fb3-121">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="c0fb3-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c0fb3-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c0fb3-123">**visKeepTextFlat**</span><span class="sxs-lookup"><span data-stu-id="c0fb3-123">**visKeepTextFlat**</span></span> <br/> |
   

