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
ms.openlocfilehash: 607881e4a520f1376562394c6e40ab5d2508906d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430258"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a><span data-ttu-id="9fd06-103">ShapeShdwType Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="9fd06-103">ShapeShdwType Cell (Fill Format Section)</span></span>

<span data-ttu-id="9fd06-104">Indique le type d'ombre d'une forme.</span><span class="sxs-lookup"><span data-stu-id="9fd06-104">Specifies the type of shadow for a shape.</span></span> 
  
|<span data-ttu-id="9fd06-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9fd06-105">**Value**</span></span>|<span data-ttu-id="9fd06-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="9fd06-106">**Description**</span></span>|<span data-ttu-id="9fd06-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="9fd06-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9fd06-108">0</span><span class="sxs-lookup"><span data-stu-id="9fd06-108">0</span></span>  <br/> |<span data-ttu-id="9fd06-109">Utiliser la valeur par défaut de la page (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="9fd06-109">Use page default (the default)</span></span>  <br/> |<span data-ttu-id="9fd06-110">**visFSTPageDefault**</span><span class="sxs-lookup"><span data-stu-id="9fd06-110">**visFSTPageDefault**</span></span> <br/> |
|<span data-ttu-id="9fd06-111">1</span><span class="sxs-lookup"><span data-stu-id="9fd06-111">1</span></span>  <br/> |<span data-ttu-id="9fd06-112">Simple</span><span class="sxs-lookup"><span data-stu-id="9fd06-112">Simple</span></span>  <br/> |<span data-ttu-id="9fd06-113">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="9fd06-113">**visFSTSimple**</span></span> <br/> |
|<span data-ttu-id="9fd06-114">2</span><span class="sxs-lookup"><span data-stu-id="9fd06-114">2</span></span>  <br/> |<span data-ttu-id="9fd06-115">Oblique</span><span class="sxs-lookup"><span data-stu-id="9fd06-115">Oblique</span></span>  <br/> |<span data-ttu-id="9fd06-116">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="9fd06-116">**visFSTOblique**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fd06-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="9fd06-117">Remarks</span></span>

<span data-ttu-id="9fd06-118">Utilisez cette cellule pour appliquer une ombre de forme différente de la page par défaut (le type d’ombre par défaut de la page est défini dans la cellule ShdwType de la section Page Properties).</span><span class="sxs-lookup"><span data-stu-id="9fd06-118">Use this cell to apply a shape shadow that is different from the page default (the page default shadow type is defined in the ShdwType cell in the Page Properties Section).</span></span>
  
<span data-ttu-id="9fd06-119">Les ombres simples sont décrites comme des ombres de décalage dans l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9fd06-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="9fd06-120">Une ombre simple donne l'impression que la forme a son ombre portée sur un plan parallèle situé derrière elle.</span><span class="sxs-lookup"><span data-stu-id="9fd06-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located behind the shape.</span></span> <span data-ttu-id="9fd06-121">Les ombres obliques sont décrites comme telles dans l'interface utilisateur et donnent l'impression d'une ombre portée sur un plan perpendiculaire à la forme.</span><span class="sxs-lookup"><span data-stu-id="9fd06-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="9fd06-122">Pour obtenir une liste de types d’ombre simples et obliques prédéfinis, reportez-vous à la zone **Style** dans la boîte de dialogue **Ombre** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Ombre**, puis cliquez sur **Options d’ombres**).</span><span class="sxs-lookup"><span data-stu-id="9fd06-122">For a list of predefined simple and oblique shadow types, see the **Style** box in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="9fd06-123">Pour obtenir une référence à la cellule ShapeShdwType par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9fd06-123">To get a reference to the ShapeShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9fd06-124">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="9fd06-124">Cell name:</span></span>  <br/> |<span data-ttu-id="9fd06-125">ShapeShdwType</span><span class="sxs-lookup"><span data-stu-id="9fd06-125">ShapeShdwType</span></span>  <br/> |
   
<span data-ttu-id="9fd06-126">Pour obtenir une référence à la cellule ShapeShdwType à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9fd06-126">To get a reference to the ShapeShdwType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9fd06-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9fd06-127">Section index:</span></span>  <br/> |<span data-ttu-id="9fd06-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9fd06-128">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9fd06-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9fd06-129">Row index:</span></span>  <br/> |<span data-ttu-id="9fd06-130">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="9fd06-130">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="9fd06-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9fd06-131">Cell index:</span></span>  <br/> |<span data-ttu-id="9fd06-132">**visFillShdwType**</span><span class="sxs-lookup"><span data-stu-id="9fd06-132">**visFillShdwType**</span></span> <br/> |
   

