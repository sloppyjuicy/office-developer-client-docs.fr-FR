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
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788048"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="75dfe-103">BeginGroup, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="75dfe-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="75dfe-104">Indique si un séparateur est inséré dans le menu au-dessus de cette action.</span><span class="sxs-lookup"><span data-stu-id="75dfe-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="75dfe-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="75dfe-105">**Value**</span></span>|<span data-ttu-id="75dfe-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="75dfe-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75dfe-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="75dfe-107">TRUE</span></span>  <br/> |<span data-ttu-id="75dfe-108">Un séparateur est inséré dans le menu au-dessus de cette action.</span><span class="sxs-lookup"><span data-stu-id="75dfe-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="75dfe-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="75dfe-109">FALSE</span></span>  <br/> |<span data-ttu-id="75dfe-110">Un séparateur n’est pas inséré dans le menu au-dessus de cette action (la valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="75dfe-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75dfe-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="75dfe-111">Remarks</span></span>

<span data-ttu-id="75dfe-112">Pour obtenir une référence à la cellule BeginGroup par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="75dfe-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75dfe-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="75dfe-113">Cell name:</span></span>  <br/> |<span data-ttu-id="75dfe-114">Actions.</span><span class="sxs-lookup"><span data-stu-id="75dfe-114">Actions.</span></span> <span data-ttu-id="75dfe-115">*nom*. BeginGroup où Actions.</span><span class="sxs-lookup"><span data-stu-id="75dfe-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="75dfe-116">*nom* est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="75dfe-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="75dfe-117">Pour obtenir une référence à la cellule BeginGroup par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="75dfe-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75dfe-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="75dfe-118">Section index:</span></span>  <br/> |<span data-ttu-id="75dfe-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="75dfe-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="75dfe-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="75dfe-120">Row index:</span></span>  <br/> |<span data-ttu-id="75dfe-121">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="75dfe-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="75dfe-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="75dfe-122">Cell index:</span></span>  <br/> |<span data-ttu-id="75dfe-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="75dfe-123">**visActionBeginGroup**</span></span> <br/> |
   

