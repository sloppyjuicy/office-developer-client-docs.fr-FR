---
title: ShdwType, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Indique le type d'ombre par défaut d'une page.
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342888"
---
# <a name="shdwtype-cell-page-properties-section"></a><span data-ttu-id="4aaf3-103">ShdwType, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="4aaf3-103">ShdwType Cell (Page Properties Section)</span></span>

<span data-ttu-id="4aaf3-104">Indique le type d'ombre par défaut d'une page.</span><span class="sxs-lookup"><span data-stu-id="4aaf3-104">Indicates the default shadow type for a page.</span></span>
  
|<span data-ttu-id="4aaf3-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="4aaf3-105">**Value**</span></span>|<span data-ttu-id="4aaf3-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="4aaf3-106">**Description**</span></span>|<span data-ttu-id="4aaf3-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="4aaf3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4aaf3-108">0,1</span><span class="sxs-lookup"><span data-stu-id="4aaf3-108">1</span></span>  <br/> | <span data-ttu-id="4aaf3-109">Simple</span><span class="sxs-lookup"><span data-stu-id="4aaf3-109">Simple</span></span>  <br/> |<span data-ttu-id="4aaf3-110">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="4aaf3-110">**visFSTSimple**</span></span> <br/> |
| <span data-ttu-id="4aaf3-111">n°2</span><span class="sxs-lookup"><span data-stu-id="4aaf3-111">2</span></span>  <br/> | <span data-ttu-id="4aaf3-112">Italique</span><span class="sxs-lookup"><span data-stu-id="4aaf3-112">Oblique</span></span>  <br/> |<span data-ttu-id="4aaf3-113">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="4aaf3-113">**visFSTOblique**</span></span> <br/> |
|<span data-ttu-id="4aaf3-114">3</span><span class="sxs-lookup"><span data-stu-id="4aaf3-114">3</span></span>  <br/> |<span data-ttu-id="4aaf3-115">Intérieur</span><span class="sxs-lookup"><span data-stu-id="4aaf3-115">Inner</span></span>  <br/> |<span data-ttu-id="4aaf3-116">**visFSTInner**</span><span class="sxs-lookup"><span data-stu-id="4aaf3-116">**visFSTInner**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4aaf3-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="4aaf3-117">Remarks</span></span>

 <span data-ttu-id="4aaf3-118">Le type d'ombre décrit dans cette cellule est utilisé chaque fois que la cellule ShapeShdwType (le type d'ombre d'une forme individuelle sur la page) est définie sur page default (**visFSTPageDefault** ).</span><span class="sxs-lookup"><span data-stu-id="4aaf3-118">The shadow type described in this cell is used whenever the ShapeShdwType Cell (the shadow type for an individual shape on the page) is set to Page Default (**visFSTPageDefault** ).</span></span> 
  
<span data-ttu-id="4aaf3-119">Les ombres simples sont décrites comme des ombres de décalage dans l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4aaf3-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="4aaf3-120">Une ombre simple donne l'impression que la forme a son ombre portée sur un plan parallèle situé à une certaine distance derrière elle.</span><span class="sxs-lookup"><span data-stu-id="4aaf3-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located some distance behind it.</span></span> <span data-ttu-id="4aaf3-121">Les ombres obliques sont décrites comme telles dans l'interface utilisateur et donnent l'impression d'une ombre portée sur un plan perpendiculaire à la forme.</span><span class="sxs-lookup"><span data-stu-id="4aaf3-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="4aaf3-122">Pour obtenir une liste des types d’ombre simples et obliques prédéfinis, reportez-vous à la liste **Style** sous l’onglet **Ombres** de la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**).</span><span class="sxs-lookup"><span data-stu-id="4aaf3-122">For a list of predefined simple and oblique shadow types, see the **Style** list on the **Shadows** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="4aaf3-123">Pour obtenir une référence à la cellule ShdwType par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="4aaf3-123">To get a reference to the ShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4aaf3-124">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="4aaf3-124">Cell name:</span></span>  <br/> | <span data-ttu-id="4aaf3-125">ShdwType</span><span class="sxs-lookup"><span data-stu-id="4aaf3-125">ShdwType</span></span>  <br/> |
   
<span data-ttu-id="4aaf3-126">Pour obtenir une référence à la cellule ShdwType par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="4aaf3-126">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4aaf3-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="4aaf3-127">Section index:</span></span>  <br/> |<span data-ttu-id="4aaf3-128">**Définis**</span><span class="sxs-lookup"><span data-stu-id="4aaf3-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4aaf3-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="4aaf3-129">Row index:</span></span>  <br/> |<span data-ttu-id="4aaf3-130">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="4aaf3-130">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="4aaf3-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4aaf3-131">Cell index:</span></span>  <br/> |<span data-ttu-id="4aaf3-132">**visPageShdwType**</span><span class="sxs-lookup"><span data-stu-id="4aaf3-132">**visPageShdwType**</span></span> <br/> |
   

