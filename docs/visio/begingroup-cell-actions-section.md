---
title: BeginGroup, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Indique si un séparateur est inséré dans le menu au-dessus de cette action.
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407836"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="d17c1-103">BeginGroup, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="d17c1-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="d17c1-104">Indique si un séparateur est inséré dans le menu au-dessus de cette action.</span><span class="sxs-lookup"><span data-stu-id="d17c1-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="d17c1-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="d17c1-105">**Value**</span></span>|<span data-ttu-id="d17c1-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="d17c1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d17c1-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d17c1-107">TRUE</span></span>  <br/> |<span data-ttu-id="d17c1-108">Un séparateur est inséré dans le menu au-dessus de cette action.</span><span class="sxs-lookup"><span data-stu-id="d17c1-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="d17c1-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d17c1-109">FALSE</span></span>  <br/> |<span data-ttu-id="d17c1-110">Aucun séparateur n'est inséré dans le menu au-dessus de cette action (la valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="d17c1-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d17c1-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="d17c1-111">Remarks</span></span>

<span data-ttu-id="d17c1-112">Pour obtenir une référence à la cellule BeginGroup par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d17c1-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d17c1-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="d17c1-113">Cell name:</span></span>  <br/> |<span data-ttu-id="d17c1-114">Mesures.</span><span class="sxs-lookup"><span data-stu-id="d17c1-114">Actions.</span></span> <span data-ttu-id="d17c1-115">*nom*. BeginGroup, où actions.</span><span class="sxs-lookup"><span data-stu-id="d17c1-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="d17c1-116">*nom* est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="d17c1-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="d17c1-117">Pour obtenir une référence à la cellule BeginGroup à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d17c1-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d17c1-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d17c1-118">Section index:</span></span>  <br/> |<span data-ttu-id="d17c1-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="d17c1-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="d17c1-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d17c1-120">Row index:</span></span>  <br/> |<span data-ttu-id="d17c1-121">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d17c1-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d17c1-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d17c1-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d17c1-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="d17c1-123">**visActionBeginGroup**</span></span> <br/> |
   

