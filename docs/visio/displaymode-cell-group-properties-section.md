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
ms.openlocfilehash: a49d7a38eac75a2845de0ca3ad22f7cbf79a63df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413184"
---
# <a name="displaymode-cell-group-properties-section"></a><span data-ttu-id="8faff-103">DisplayMode, cellule (section Group Properties)</span><span class="sxs-lookup"><span data-stu-id="8faff-103">DisplayMode Cell (Group Properties Section)</span></span>

<span data-ttu-id="8faff-104">Détermine le mode d'affichage de la forme de groupe et de ses membres.</span><span class="sxs-lookup"><span data-stu-id="8faff-104">Determines how the group shape and its members are displayed.</span></span>
  
|<span data-ttu-id="8faff-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8faff-105">**Value**</span></span>|<span data-ttu-id="8faff-106">**Mode d’affichage**</span><span class="sxs-lookup"><span data-stu-id="8faff-106">**Display Mode**</span></span>|<span data-ttu-id="8faff-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="8faff-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8faff-108">0</span><span class="sxs-lookup"><span data-stu-id="8faff-108">0</span></span>  <br/> |<span data-ttu-id="8faff-109">Masque la forme de groupe et le texte</span><span class="sxs-lookup"><span data-stu-id="8faff-109">Hides the group shape and text.</span></span>  <br/> |<span data-ttu-id="8faff-110">**visGrpDispModeNone**</span><span class="sxs-lookup"><span data-stu-id="8faff-110">**visGrpDispModeNone**</span></span> <br/> |
|<span data-ttu-id="8faff-111">1 </span><span class="sxs-lookup"><span data-stu-id="8faff-111">1</span></span>  <br/> |<span data-ttu-id="8faff-112">Affiche la forme de groupe derrière ses membres</span><span class="sxs-lookup"><span data-stu-id="8faff-112">Displays the group shape behind member shapes.</span></span>  <br/> |<span data-ttu-id="8faff-113">**visGrpDispModeBack**</span><span class="sxs-lookup"><span data-stu-id="8faff-113">**visGrpDispModeBack**</span></span> <br/> |
|<span data-ttu-id="8faff-114">2 </span><span class="sxs-lookup"><span data-stu-id="8faff-114">2</span></span>  <br/> |<span data-ttu-id="8faff-115">Affiche la forme de groupe devant ses membres</span><span class="sxs-lookup"><span data-stu-id="8faff-115">Displays the group shape in front of member shapes.</span></span>  <br/> |<span data-ttu-id="8faff-116">**visGrpDispModeFront**</span><span class="sxs-lookup"><span data-stu-id="8faff-116">**visGrpDispModeFront**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8faff-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="8faff-117">Remarks</span></span>

<span data-ttu-id="8faff-118">Vous pouvez également définir cette valeur en  sélectionnant  le groupe, [](run-in-developer-mode-display-the-developer-tab.md) en cliquant sur Comportement dans le groupe Création de forme sous l’onglet Développeur, puis en sélectionnant un mode d’affichage dans la liste de données **de** groupe.</span><span class="sxs-lookup"><span data-stu-id="8faff-118">You can also set this value by selecting the group, clicking **Behavior** on the **Shape Design** group on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, and then selecting a display mode from the **Group data** list.</span></span> 
  
<span data-ttu-id="8faff-119">Pour obtenir une référence à la cellule DisplayMode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="8faff-119">To get a reference to the DisplayMode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8faff-120">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="8faff-120">Cell name:</span></span>  <br/> |<span data-ttu-id="8faff-121">DisplayMode</span><span class="sxs-lookup"><span data-stu-id="8faff-121">DisplayMode</span></span>  <br/> |
   
<span data-ttu-id="8faff-122">Pour obtenir une référence à la cellule DisplayMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8faff-122">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8faff-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8faff-123">Section index:</span></span>  <br/> |<span data-ttu-id="8faff-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8faff-124">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8faff-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8faff-125">Row index:</span></span>  <br/> |<span data-ttu-id="8faff-126">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="8faff-126">**visRowGroup**</span></span> <br/> |
|<span data-ttu-id="8faff-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8faff-127">Cell index:</span></span>  <br/> |<span data-ttu-id="8faff-128">**visGroupDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="8faff-128">**visGroupDisplayMode**</span></span> <br/> |
   

