---
title: Can Glue, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Détermine si une poignée de contrôle peut être collée à d'autres formes.
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788176"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="b0e8c-103">Can Glue, cellule (section Controls)</span><span class="sxs-lookup"><span data-stu-id="b0e8c-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="b0e8c-104">Détermine si une poignée de contrôle peut être collée à d'autres formes.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="b0e8c-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b0e8c-105">**Value**</span></span>|<span data-ttu-id="b0e8c-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b0e8c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b0e8c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b0e8c-107">TRUE</span></span>  <br/> | <span data-ttu-id="b0e8c-108">La poignée de contrôle peut être collée.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="b0e8c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b0e8c-109">FALSE</span></span>  <br/> | <span data-ttu-id="b0e8c-110">La poignée de contrôle ne peut pas être collée.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0e8c-111">Note</span><span class="sxs-lookup"><span data-stu-id="b0e8c-111">Remarks</span></span>

<span data-ttu-id="b0e8c-112">Pour obtenir une référence à la cellule Can Glue par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="b0e8c-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b0e8c-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b0e8c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b0e8c-114">Contrôles.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-114">Controls.</span></span>  <span data-ttu-id="b0e8c-115">*nom* . Contrôles CanGluewhere.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="b0e8c-116">*nom* est le nom de la ligne des contrôles.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="b0e8c-117">Pour obtenir une référence à la cellule Can Glue par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b0e8c-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b0e8c-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b0e8c-118">Section index:</span></span>  <br/> |<span data-ttu-id="b0e8c-119">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="b0e8c-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="b0e8c-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b0e8c-120">Row index:</span></span>  <br/> |<span data-ttu-id="b0e8c-121">**visRowControl** +  *i* où *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="b0e8c-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="b0e8c-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b0e8c-122">Cell index:</span></span>  <br/> |<span data-ttu-id="b0e8c-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="b0e8c-123">**visCtlGlue**</span></span> <br/> |
   

