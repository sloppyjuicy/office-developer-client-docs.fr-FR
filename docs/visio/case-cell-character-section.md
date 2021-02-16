---
title: Case, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Détermine la casse du texte de la forme. Toutes les lettres capitales (majuscules) (1) et Capitales initiales uniquement (2) ne modifient pas l'apparence d'un texte qui a été entré tout en lettres capitales. Le texte doit avoir été entré en lettres minuscules pour que les effets de cette option soient visibles.
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434346"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="63ce4-105">Case, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="63ce4-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="63ce4-p102">Détermine la casse du texte de la forme. Toutes les lettres capitales (majuscules) (1) et Capitales initiales uniquement (2) ne modifient pas l'apparence d'un texte qui a été entré tout en lettres capitales. Le texte doit avoir été entré en lettres minuscules pour que les effets de cette option soient visibles.</span><span class="sxs-lookup"><span data-stu-id="63ce4-p102">Determines the case of a shape's text. All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters. The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="63ce4-109">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="63ce4-109">**Value**</span></span>|<span data-ttu-id="63ce4-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="63ce4-110">**Description**</span></span>|<span data-ttu-id="63ce4-111">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="63ce4-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="63ce4-112">0</span><span class="sxs-lookup"><span data-stu-id="63ce4-112">0</span></span>  <br/> | <span data-ttu-id="63ce4-113">Casse normale</span><span class="sxs-lookup"><span data-stu-id="63ce4-113">Normal case</span></span>  <br/> |<span data-ttu-id="63ce4-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="63ce4-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="63ce4-115">1 </span><span class="sxs-lookup"><span data-stu-id="63ce4-115">1</span></span>  <br/> | <span data-ttu-id="63ce4-116">Toutes les lettres en capitales (majuscules)</span><span class="sxs-lookup"><span data-stu-id="63ce4-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="63ce4-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="63ce4-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="63ce4-118">2 </span><span class="sxs-lookup"><span data-stu-id="63ce4-118">2</span></span>  <br/> | <span data-ttu-id="63ce4-119">Capitales initiales uniquement</span><span class="sxs-lookup"><span data-stu-id="63ce4-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="63ce4-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="63ce4-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63ce4-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="63ce4-121">Remarks</span></span>

<span data-ttu-id="63ce4-122">Pour obtenir une référence à la cellule Case par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="63ce4-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="63ce4-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="63ce4-123">Cell name:</span></span>  <br/> | <span data-ttu-id="63ce4-124">Char.Case[  *i*  ] où  *i*  = <1>, 2, 3, ...</span><span class="sxs-lookup"><span data-stu-id="63ce4-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="63ce4-125">Pour obtenir une référence à la cellule Case à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="63ce4-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="63ce4-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="63ce4-126">Section index:</span></span>  <br/> |<span data-ttu-id="63ce4-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="63ce4-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="63ce4-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="63ce4-128">Row index:</span></span>  <br/> |<span data-ttu-id="63ce4-129">**visRowCharacter**  +   *i* où *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="63ce4-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="63ce4-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="63ce4-130">Cell index:</span></span>  <br/> |<span data-ttu-id="63ce4-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="63ce4-131">**visCharacterCase**</span></span> <br/> |
   

