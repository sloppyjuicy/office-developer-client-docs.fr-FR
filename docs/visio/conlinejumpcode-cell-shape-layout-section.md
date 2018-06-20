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
ms.openlocfilehash: 002f628841356ec8a22afbb9d4aeca8236058222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788335"
---
# <a name="conlinejumpcode-cell-shape-layout-section"></a><span data-ttu-id="6e432-103">ConLineJumpCode, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="6e432-103">ConLineJumpCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="6e432-104">Détermine la déviation des traits de connecteurs.</span><span class="sxs-lookup"><span data-stu-id="6e432-104">Determines when a connector jumps.</span></span>
  
|<span data-ttu-id="6e432-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="6e432-105">**Value**</span></span>|<span data-ttu-id="6e432-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="6e432-106">**Description**</span></span>|<span data-ttu-id="6e432-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="6e432-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6e432-108">0</span><span class="sxs-lookup"><span data-stu-id="6e432-108">0</span></span>  <br/> |<span data-ttu-id="6e432-109">Selon la page ; sous l’onglet **Création** , cliquez sur la flèche dans le groupe **Mise en Page** , puis cliquez sur l’onglet **disposition et positionnement** pour afficher les spécifications de la page</span><span class="sxs-lookup"><span data-stu-id="6e432-109">As page specifies; on the **Design** tab, click the arrow in the **Page Setup** group, and then click the **Layout and Routing** tab to see the page specifications</span></span>  <br/> |<span data-ttu-id="6e432-110">**visSLOJumpDefault**</span><span class="sxs-lookup"><span data-stu-id="6e432-110">**visSLOJumpDefault**</span></span> <br/> |
|<span data-ttu-id="6e432-111">1</span><span class="sxs-lookup"><span data-stu-id="6e432-111">1</span></span>  <br/> |<span data-ttu-id="6e432-112">Jamais</span><span class="sxs-lookup"><span data-stu-id="6e432-112">Never</span></span>  <br/> |<span data-ttu-id="6e432-113">**visSLOJumpNever**</span><span class="sxs-lookup"><span data-stu-id="6e432-113">**visSLOJumpNever**</span></span> <br/> |
|<span data-ttu-id="6e432-114">2</span><span class="sxs-lookup"><span data-stu-id="6e432-114">2</span></span>  <br/> |<span data-ttu-id="6e432-115">Always (Toujours)</span><span class="sxs-lookup"><span data-stu-id="6e432-115">Always</span></span>  <br/> |<span data-ttu-id="6e432-116">**visSLOJumpAlways**</span><span class="sxs-lookup"><span data-stu-id="6e432-116">**visSLOJumpAlways**</span></span> <br/> |
|<span data-ttu-id="6e432-117">3</span><span class="sxs-lookup"><span data-stu-id="6e432-117">3</span></span>  <br/> |<span data-ttu-id="6e432-118">L'autre connecteur est dévié</span><span class="sxs-lookup"><span data-stu-id="6e432-118">Other connector jumps</span></span>  <br/> |<span data-ttu-id="6e432-119">**visSLOJumpOther**</span><span class="sxs-lookup"><span data-stu-id="6e432-119">**visSLOJumpOther**</span></span> <br/> |
|<span data-ttu-id="6e432-120">4</span><span class="sxs-lookup"><span data-stu-id="6e432-120">4</span></span>  <br/> |<span data-ttu-id="6e432-121">Aucun connecteur n’est dévié</span><span class="sxs-lookup"><span data-stu-id="6e432-121">Neither connector jumps</span></span>  <br/> |<span data-ttu-id="6e432-122">**visSLOJumpNeither**</span><span class="sxs-lookup"><span data-stu-id="6e432-122">**visSLOJumpNeither**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e432-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e432-123">Remarks</span></span>

<span data-ttu-id="6e432-124">Vous pouvez également définir la valeur de cette cellule en sélectionnant un connecteur dynamique et en cliquant sur **comportement** dans le groupe **Création de la forme** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis en cliquant sur l’onglet **connecteur** .</span><span class="sxs-lookup"><span data-stu-id="6e432-124">You can also set the value of this cell by selecting a dynamic connector, clicking **Behavior** in the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then clicking the **Connector** tab.</span></span> 
  
<span data-ttu-id="6e432-125">Pour obtenir une référence à la cellule ConLineJumpCode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="6e432-125">To get a reference to the ConLineJumpCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e432-126">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6e432-126">Cell name:</span></span>  <br/> |<span data-ttu-id="6e432-127">ConLineJumpCode</span><span class="sxs-lookup"><span data-stu-id="6e432-127">ConLineJumpCode</span></span>  <br/> |
   
<span data-ttu-id="6e432-128">Pour obtenir une référence à la cellule ConLineJumpCode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="6e432-128">To get a reference to the ConLineJumpCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e432-129">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6e432-129">Section index:</span></span>  <br/> |<span data-ttu-id="6e432-130">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6e432-130">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6e432-131">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6e432-131">Row index:</span></span>  <br/> |<span data-ttu-id="6e432-132">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="6e432-132">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="6e432-133">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6e432-133">Cell index:</span></span>  <br/> |<span data-ttu-id="6e432-134">**visSLOJumpCode**</span><span class="sxs-lookup"><span data-stu-id="6e432-134">**visSLOJumpCode**</span></span> <br/> |
   

