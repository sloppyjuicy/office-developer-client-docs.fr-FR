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
ms.openlocfilehash: 1fc5c31a723d5d409110d94ff543a45dadabf264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789713"
---
# <a name="shdwtype-cell-page-properties-section"></a><span data-ttu-id="d2074-103">ShdwType, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="d2074-103">ShdwType Cell (Page Properties Section)</span></span>

<span data-ttu-id="d2074-104">Indique le type d'ombre par défaut d'une page.</span><span class="sxs-lookup"><span data-stu-id="d2074-104">Indicates the default shadow type for a page.</span></span>
  
|<span data-ttu-id="d2074-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="d2074-105">**Value**</span></span>|<span data-ttu-id="d2074-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="d2074-106">**Description**</span></span>|<span data-ttu-id="d2074-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="d2074-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d2074-108">1</span><span class="sxs-lookup"><span data-stu-id="d2074-108">1</span></span>  <br/> | <span data-ttu-id="d2074-109">Simple</span><span class="sxs-lookup"><span data-stu-id="d2074-109">Simple</span></span>  <br/> |<span data-ttu-id="d2074-110">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="d2074-110">**visFSTSimple**</span></span> <br/> |
| <span data-ttu-id="d2074-111">2</span><span class="sxs-lookup"><span data-stu-id="d2074-111">2</span></span>  <br/> | <span data-ttu-id="d2074-112">Oblique</span><span class="sxs-lookup"><span data-stu-id="d2074-112">Oblique</span></span>  <br/> |<span data-ttu-id="d2074-113">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="d2074-113">**visFSTOblique**</span></span> <br/> |
|<span data-ttu-id="d2074-114">3</span><span class="sxs-lookup"><span data-stu-id="d2074-114">3</span></span>  <br/> |<span data-ttu-id="d2074-115">Interne</span><span class="sxs-lookup"><span data-stu-id="d2074-115">Inner</span></span>  <br/> |<span data-ttu-id="d2074-116">**visFSTInner**</span><span class="sxs-lookup"><span data-stu-id="d2074-116">**visFSTInner**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2074-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2074-117">Remarks</span></span>

 <span data-ttu-id="d2074-118">Le type d’ombre décrit dans cette cellule est utilisé chaque fois que la cellule ShapeShdwType (le type d’ombre d’une forme individuelle sur la page) est réglée sur Page Default (**visFSTPageDefault** ).</span><span class="sxs-lookup"><span data-stu-id="d2074-118">The shadow type described in this cell is used whenever the ShapeShdwType Cell (the shadow type for an individual shape on the page) is set to Page Default (**visFSTPageDefault** ).</span></span> 
  
<span data-ttu-id="d2074-119">Types d’ombre simple sont décrits comme des ombres décalage dans l’interface utilisateur (IU).</span><span class="sxs-lookup"><span data-stu-id="d2074-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="d2074-120">Une ombre simple donne l’effet de la forme de son ombre portée sur un plan parallèle situé certaine distance derrière elle.</span><span class="sxs-lookup"><span data-stu-id="d2074-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located some distance behind it.</span></span> <span data-ttu-id="d2074-121">Ombres obliques sont décrites comme telles dans l’interface utilisateur et donnent l’effet d’une ombre portée sur un plan perpendiculaire à la forme.</span><span class="sxs-lookup"><span data-stu-id="d2074-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="d2074-122">Pour une liste des types d’ombre simples et obliques prédéfinis, voir la liste **Style** de l’onglet **ombres** de la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ).</span><span class="sxs-lookup"><span data-stu-id="d2074-122">For a list of predefined simple and oblique shadow types, see the **Style** list on the **Shadows** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="d2074-123">Pour obtenir une référence à la cellule ShdwType par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="d2074-123">To get a reference to the ShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2074-124">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="d2074-124">Cell name:</span></span>  <br/> | <span data-ttu-id="d2074-125">ShdwType</span><span class="sxs-lookup"><span data-stu-id="d2074-125">ShdwType</span></span>  <br/> |
   
<span data-ttu-id="d2074-126">Pour obtenir une référence à la cellule ShapeShdwOffsetX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d2074-126">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2074-127">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d2074-127">Section index:</span></span>  <br/> |<span data-ttu-id="d2074-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d2074-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d2074-129">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d2074-129">Row index:</span></span>  <br/> |<span data-ttu-id="d2074-130">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="d2074-130">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="d2074-131">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d2074-131">Cell index:</span></span>  <br/> |<span data-ttu-id="d2074-132">**visPageShdwType**</span><span class="sxs-lookup"><span data-stu-id="d2074-132">**visPageShdwType**</span></span> <br/> |
   

