---
title: DisplayMode, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251623
localization_priority: Normal
ms.assetid: e6d72529-aa03-e94b-130c-79ed04336299
description: Détermine le mode d'affichage de la forme de groupe et de ses membres.
ms.openlocfilehash: 086685b47d8eaf170a8722f7cd00545230541e79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788477"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="cec75-103">DisplayMode, cellule (section Group Properties)</span><span class="sxs-lookup"><span data-stu-id="cec75-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="cec75-104">Détermine le mode d'affichage de la forme de groupe et de ses membres.</span><span class="sxs-lookup"><span data-stu-id="cec75-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="cec75-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="cec75-105">**Value**</span></span>|<span data-ttu-id="cec75-106">**Mode d’affichage**</span><span class="sxs-lookup"><span data-stu-id="cec75-106">**Display Mode**</span></span>|<span data-ttu-id="cec75-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="cec75-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cec75-108">0</span><span class="sxs-lookup"><span data-stu-id="cec75-108">0</span></span>  <br/> |<span data-ttu-id="cec75-109">Masque la forme de groupe et le texte</span><span class="sxs-lookup"><span data-stu-id="cec75-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="cec75-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="cec75-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="cec75-111">1</span><span class="sxs-lookup"><span data-stu-id="cec75-111">1</span></span>  <br/> |<span data-ttu-id="cec75-112">Affiche la forme de groupe derrière ses membres</span><span class="sxs-lookup"><span data-stu-id="cec75-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="cec75-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="cec75-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="cec75-114">2</span><span class="sxs-lookup"><span data-stu-id="cec75-114">2</span></span>  <br/> |<span data-ttu-id="cec75-115">Affiche la forme de groupe devant ses membres</span><span class="sxs-lookup"><span data-stu-id="cec75-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="cec75-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="cec75-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cec75-117">Note</span><span class="sxs-lookup"><span data-stu-id="cec75-117">Remarks</span></span>

<span data-ttu-id="cec75-118">Vous pouvez également définir cette valeur sélectionnant le groupe, en cliquant sur **comportement** dans le groupe **Création de la forme** sous l’onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , puis en sélectionnant un mode d’affichage de la liste de **données de groupe** .</span><span class="sxs-lookup"><span data-stu-id="cec75-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="cec75-119">Pour obtenir une référence à la cellule DisplayMode par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="cec75-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cec75-120">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="cec75-120">Cell name:</span></span>  <br/> |<span data-ttu-id="cec75-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="cec75-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="cec75-122">Pour obtenir une référence à la cellule DisplayMode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="cec75-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cec75-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="cec75-123">Section index:</span></span>  <br/> |<span data-ttu-id="cec75-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cec75-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cec75-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="cec75-125">Row index:</span></span>  <br/> |<span data-ttu-id="cec75-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="cec75-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="cec75-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="cec75-127">Cell index:</span></span>  <br/> |<span data-ttu-id="cec75-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="cec75-128">**visGroupDisplayMode**</span></span> <br/> |
   

