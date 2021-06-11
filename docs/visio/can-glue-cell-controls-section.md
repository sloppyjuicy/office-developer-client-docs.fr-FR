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
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423292"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="5de0f-103">Can Glue, cellule (section Controls)</span><span class="sxs-lookup"><span data-stu-id="5de0f-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="5de0f-104">Détermine si une poignée de contrôle peut être collée à d'autres formes.</span><span class="sxs-lookup"><span data-stu-id="5de0f-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="5de0f-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5de0f-105">**Value**</span></span>|<span data-ttu-id="5de0f-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="5de0f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5de0f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5de0f-107">TRUE</span></span>  <br/> | <span data-ttu-id="5de0f-108">La poignée de contrôle peut être collée.</span><span class="sxs-lookup"><span data-stu-id="5de0f-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="5de0f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5de0f-109">FALSE</span></span>  <br/> | <span data-ttu-id="5de0f-110">La poignée de contrôle ne peut pas être collée.</span><span class="sxs-lookup"><span data-stu-id="5de0f-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5de0f-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="5de0f-111">Remarks</span></span>

<span data-ttu-id="5de0f-112">Pour obtenir une référence à la cellule Can Glue par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="5de0f-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5de0f-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5de0f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="5de0f-114">Contrôles.</span><span class="sxs-lookup"><span data-stu-id="5de0f-114">Controls.</span></span>  <span data-ttu-id="5de0f-115">*nom*  . Contrôles CanGluewhere.</span><span class="sxs-lookup"><span data-stu-id="5de0f-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="5de0f-116">*nom*  est le nom de la ligne des contrôles.</span><span class="sxs-lookup"><span data-stu-id="5de0f-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="5de0f-117">Pour obtenir une référence à la cellule Can Glue à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5de0f-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5de0f-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5de0f-118">Section index:</span></span>  <br/> |<span data-ttu-id="5de0f-119">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="5de0f-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="5de0f-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5de0f-120">Row index:</span></span>  <br/> |<span data-ttu-id="5de0f-121">**visRowControl**  +   *i* où *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="5de0f-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="5de0f-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5de0f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="5de0f-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="5de0f-123">**visCtlGlue**</span></span> <br/> |
   

