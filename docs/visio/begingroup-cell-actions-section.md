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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361032"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="a7d49-103">BeginGroup, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="a7d49-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="a7d49-104">Indique si un séparateur est inséré dans le menu au-dessus de cette action.</span><span class="sxs-lookup"><span data-stu-id="a7d49-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="a7d49-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="a7d49-105">**Value**</span></span>|<span data-ttu-id="a7d49-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="a7d49-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7d49-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a7d49-107">TRUE</span></span>  <br/> |<span data-ttu-id="a7d49-108">Un séparateur est inséré dans le menu au-dessus de cette action.</span><span class="sxs-lookup"><span data-stu-id="a7d49-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="a7d49-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a7d49-109">FALSE</span></span>  <br/> |<span data-ttu-id="a7d49-110">Aucun séparateur n'est inséré dans le menu au-dessus de cette action (la valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="a7d49-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7d49-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7d49-111">Remarks</span></span>

<span data-ttu-id="a7d49-112">Pour obtenir une référence à la cellule BeginGroup par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="a7d49-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7d49-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="a7d49-113">Cell name:</span></span>  <br/> |<span data-ttu-id="a7d49-114">Mesures.</span><span class="sxs-lookup"><span data-stu-id="a7d49-114">Actions.</span></span> <span data-ttu-id="a7d49-115">*nom*. BeginGroup, où actions.</span><span class="sxs-lookup"><span data-stu-id="a7d49-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="a7d49-116">*nom* est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="a7d49-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="a7d49-117">Pour obtenir une référence à la cellule BeginGroup à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a7d49-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7d49-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a7d49-118">Section index:</span></span>  <br/> |<span data-ttu-id="a7d49-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="a7d49-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="a7d49-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a7d49-120">Row index:</span></span>  <br/> |<span data-ttu-id="a7d49-121">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a7d49-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a7d49-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a7d49-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a7d49-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="a7d49-123">**visActionBeginGroup**</span></span> <br/> |
   

