---
title: ObjectKind, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Indique le type de champ de texte.
ms.openlocfilehash: c2f891620f704a3c48861124b886e49d356960ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360990"
---
# <a name="objectkind-cell-text-fields-section"></a><span data-ttu-id="b3dae-103">ObjectKind, cellule (section Text Fields)</span><span class="sxs-lookup"><span data-stu-id="b3dae-103">ObjectKind Cell (Text Fields Section)</span></span>

<span data-ttu-id="b3dae-104">Indique le type de champ de texte.</span><span class="sxs-lookup"><span data-stu-id="b3dae-104">Indicates the type of text field.</span></span>
  
|<span data-ttu-id="b3dae-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="b3dae-105">**Value**</span></span>|<span data-ttu-id="b3dae-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b3dae-106">**Description**</span></span>|<span data-ttu-id="b3dae-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="b3dae-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b3dae-108">0</span><span class="sxs-lookup"><span data-stu-id="b3dae-108">0</span></span>  <br/> | <span data-ttu-id="b3dae-109">Standard</span><span class="sxs-lookup"><span data-stu-id="b3dae-109">Standard</span></span>  <br/> |<span data-ttu-id="b3dae-110">**visTFOKStandard**</span><span class="sxs-lookup"><span data-stu-id="b3dae-110">**visTFOKStandard**</span></span> <br/> |
| <span data-ttu-id="b3dae-111">0,1</span><span class="sxs-lookup"><span data-stu-id="b3dae-111">1</span></span>  <br/> |<span data-ttu-id="b3dae-112">Horizontal en vertical</span><span class="sxs-lookup"><span data-stu-id="b3dae-112">Horizontal in vertical</span></span>  <br/> |<span data-ttu-id="b3dae-113">**visTFOKHorizontaInVertical**</span><span class="sxs-lookup"><span data-stu-id="b3dae-113">**visTFOKHorizontaInVertical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3dae-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b3dae-114">Remarks</span></span>

<span data-ttu-id="b3dae-115">Les champs de texte peuvent présenter l'un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="b3dae-115">Text fields can be one of the following types:</span></span>
  
- <span data-ttu-id="b3dae-116">standard, indiquant que le champ a été inséré par catégorie de champ ;</span><span class="sxs-lookup"><span data-stu-id="b3dae-116">Standard, indicating that the field was inserted by field category.</span></span>
    
- <span data-ttu-id="b3dae-117">horizontal en vertical, indiquant que le champ est du texte horizontal défini dans du texte vertical.</span><span class="sxs-lookup"><span data-stu-id="b3dae-117">Horizontal in vertical, indicating that the field is horizontal text set within vertical text.</span></span>
    
<span data-ttu-id="b3dae-118">Pour obtenir une référence à la cellule ObjectKind par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b3dae-118">To get a reference to the ObjectKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3dae-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b3dae-119">Cell name:</span></span>  <br/> | <span data-ttu-id="b3dae-120">Fields. ObjectKind [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b3dae-120">Fields.ObjectKind[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b3dae-121">Pour obtenir une référence à la cellule ObjectKind à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b3dae-121">To get a reference to the ObjectKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3dae-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b3dae-122">Section index:</span></span>  <br/> |<span data-ttu-id="b3dae-123">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="b3dae-123">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="b3dae-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b3dae-124">Row index:</span></span>  <br/> |<span data-ttu-id="b3dae-125">**visRowField** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b3dae-125">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b3dae-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b3dae-126">Cell index:</span></span>  <br/> |<span data-ttu-id="b3dae-127">**visFieldObjectKind**</span><span class="sxs-lookup"><span data-stu-id="b3dae-127">**visFieldObjectKind**</span></span> <br/> |
   

