---
title: ConLineJumpCode, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251652
localization_priority: Normal
ms.assetid: af85588e-8e83-5168-7a8c-d7e8b4af5c27
description: Détermine la déviation des traits de connecteurs.
ms.openlocfilehash: 28bf506b8d3729fefec438d259746661fd28586e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421619"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="dfdbc-103">ConLineJumpCode, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="dfdbc-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="dfdbc-104">Détermine la déviation des traits de connecteurs.</span><span class="sxs-lookup"><span data-stu-id="dfdbc-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="dfdbc-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="dfdbc-105">**Value**</span></span>|<span data-ttu-id="dfdbc-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="dfdbc-106">**Description**</span></span>|<span data-ttu-id="dfdbc-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="dfdbc-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dfdbc-108">0</span><span class="sxs-lookup"><span data-stu-id="dfdbc-108">0</span></span>  <br/> |<span data-ttu-id="dfdbc-109">Défini pour la page ; sous l’onglet **Création**, cliquez sur la flèche dans le groupe **Mise en page**, puis cliquez sur sur l’onglet **Disposition et positionnement** pour afficher les spécifications de la page</span><span class="sxs-lookup"><span data-stu-id="dfdbc-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="dfdbc-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="dfdbc-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="dfdbc-111">1</span><span class="sxs-lookup"><span data-stu-id="dfdbc-111">1</span></span>  <br/> |<span data-ttu-id="dfdbc-112">Jamais</span><span class="sxs-lookup"><span data-stu-id="dfdbc-112">Never</span></span>  <br/> |<span data-ttu-id="dfdbc-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="dfdbc-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="dfdbc-114">2</span><span class="sxs-lookup"><span data-stu-id="dfdbc-114">2</span></span>  <br/> |<span data-ttu-id="dfdbc-115">Toujours</span><span class="sxs-lookup"><span data-stu-id="dfdbc-115">Always</span></span>  <br/> |<span data-ttu-id="dfdbc-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="dfdbc-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="dfdbc-117">3</span><span class="sxs-lookup"><span data-stu-id="dfdbc-117">3</span></span>  <br/> |<span data-ttu-id="dfdbc-118">L'autre connecteur est dévié</span><span class="sxs-lookup"><span data-stu-id="dfdbc-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="dfdbc-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="dfdbc-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="dfdbc-120">4 </span><span class="sxs-lookup"><span data-stu-id="dfdbc-120">4</span></span>  <br/> |<span data-ttu-id="dfdbc-121">Aucun connecteur n'est dévié</span><span class="sxs-lookup"><span data-stu-id="dfdbc-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="dfdbc-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="dfdbc-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfdbc-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="dfdbc-123">Remarks</span></span>

<span data-ttu-id="dfdbc-124">Vous pouvez également définir la valeur de cette cellule  en sélectionnant un connecteur [](run-in-developer-mode-display-the-developer-tab.md) dynamique, en cliquant sur Comportement dans le groupe Création de forme sous l’onglet Développeur, puis sur l’onglet **Connecteur.** </span><span class="sxs-lookup"><span data-stu-id="dfdbc-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="dfdbc-125">Pour obtenir une référence à la cellule ConLineJumpCode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="dfdbc-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfdbc-126">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="dfdbc-126">Cell name:</span></span>  <br/> |<span data-ttu-id="dfdbc-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="dfdbc-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="dfdbc-128">Pour obtenir une référence à la cellule ConLineJumpCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dfdbc-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfdbc-129">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="dfdbc-129">Section index:</span></span>  <br/> |<span data-ttu-id="dfdbc-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dfdbc-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dfdbc-131">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="dfdbc-131">Row index:</span></span>  <br/> |<span data-ttu-id="dfdbc-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="dfdbc-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="dfdbc-133">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dfdbc-133">Cell index:</span></span>  <br/> |<span data-ttu-id="dfdbc-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="dfdbc-134">**visSLOJumpCode**</span></span> <br/> |
   

