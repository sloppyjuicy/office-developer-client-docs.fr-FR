---
title: ShapeShdwType, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: Indique le type d'ombre d'une forme.
ms.openlocfilehash: b96ad4a877d72bf4457ec3cf038a29a2b414e0f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789664"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a><span data-ttu-id="3a59c-103">ShapeShdwType, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="3a59c-103">ShapeShdwType Cell (Fill Format Section)</span></span>

<span data-ttu-id="3a59c-104">Indique le type d'ombre d'une forme.</span><span class="sxs-lookup"><span data-stu-id="3a59c-104">Specifies the type of shadow for a shape.</span></span> 
  
|<span data-ttu-id="3a59c-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3a59c-105">**Value**</span></span>|<span data-ttu-id="3a59c-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="3a59c-106">**Description**</span></span>|<span data-ttu-id="3a59c-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="3a59c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3a59c-108">0</span><span class="sxs-lookup"><span data-stu-id="3a59c-108">0</span></span>  <br/> |<span data-ttu-id="3a59c-109">Utiliser la valeur par défaut de la page (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="3a59c-109">Use page default (the default)</span></span>  <br/> |<span data-ttu-id="3a59c-110">**visFSTPageDefault**</span><span class="sxs-lookup"><span data-stu-id="3a59c-110">**visFSTPageDefault**</span></span> <br/> |
|<span data-ttu-id="3a59c-111">1</span><span class="sxs-lookup"><span data-stu-id="3a59c-111">1</span></span>  <br/> |<span data-ttu-id="3a59c-112">Simple</span><span class="sxs-lookup"><span data-stu-id="3a59c-112">Simple</span></span>  <br/> |<span data-ttu-id="3a59c-113">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="3a59c-113">**visFSTSimple**</span></span> <br/> |
|<span data-ttu-id="3a59c-114">2</span><span class="sxs-lookup"><span data-stu-id="3a59c-114">2</span></span>  <br/> |<span data-ttu-id="3a59c-115">Oblique</span><span class="sxs-lookup"><span data-stu-id="3a59c-115">Oblique</span></span>  <br/> |<span data-ttu-id="3a59c-116">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="3a59c-116">**visFSTOblique**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a59c-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="3a59c-117">Remarks</span></span>

<span data-ttu-id="3a59c-118">Utilisez cette cellule pour appliquer une ombre de la forme qui est différente de la page par défaut (le type d’ombre page par défaut est défini dans la cellule ShdwType dans la Section Page Properties).</span><span class="sxs-lookup"><span data-stu-id="3a59c-118">Use this cell to apply a shape shadow that is different from the page default (the page default shadow type is defined in the ShdwType cell in the Page Properties Section).</span></span>
  
<span data-ttu-id="3a59c-119">Types d’ombre simple sont décrits comme des ombres décalage dans l’interface utilisateur (IU).</span><span class="sxs-lookup"><span data-stu-id="3a59c-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="3a59c-120">Une ombre simple donne l’effet de la forme de son ombre portée sur un plan parallèle situé derrière la forme.</span><span class="sxs-lookup"><span data-stu-id="3a59c-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located behind the shape.</span></span> <span data-ttu-id="3a59c-121">Ombres obliques sont décrites comme telles dans l’interface utilisateur et donnent l’effet d’une ombre portée sur un plan perpendiculaire à la forme.</span><span class="sxs-lookup"><span data-stu-id="3a59c-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="3a59c-122">Pour obtenir la liste des types d’ombre simples et obliques prédéfinis, reportez-vous à la zone de **Style** dans la boîte de dialogue **ombre** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **ombre**, puis cliquez sur **Options d’ombres**).</span><span class="sxs-lookup"><span data-stu-id="3a59c-122">For a list of predefined simple and oblique shadow types, see the **Style** box in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="3a59c-123">Pour obtenir une référence à la cellule ShapeShdwType par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="3a59c-123">To get a reference to the ShapeShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a59c-124">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="3a59c-124">Cell name:</span></span>  <br/> |<span data-ttu-id="3a59c-125">ShapeShdwType</span><span class="sxs-lookup"><span data-stu-id="3a59c-125">ShapeShdwType</span></span>  <br/> |
   
<span data-ttu-id="3a59c-126">Pour obtenir une référence à la cellule ShapeShdwType par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3a59c-126">To get a reference to the ShapeShdwType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a59c-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="3a59c-127">Section index:</span></span>  <br/> |<span data-ttu-id="3a59c-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3a59c-128">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3a59c-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="3a59c-129">Row index:</span></span>  <br/> |<span data-ttu-id="3a59c-130">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="3a59c-130">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="3a59c-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3a59c-131">Cell index:</span></span>  <br/> |<span data-ttu-id="3a59c-132">**visFillShdwType**</span><span class="sxs-lookup"><span data-stu-id="3a59c-132">**visFillShdwType**</span></span> <br/> |
   

