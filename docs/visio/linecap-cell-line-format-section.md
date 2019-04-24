---
title: LineCap, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Indique si l'extrémité du trait est arrondie, carrée ou étendue.
ms.openlocfilehash: 44de4bff87fd3d121dfce9eec934ec39bc61065a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359317"
---
# <a name="linecap-cell-line-format-section"></a><span data-ttu-id="01221-103">LineCap, cellule (section Line Format)</span><span class="sxs-lookup"><span data-stu-id="01221-103">LineCap Cell (Line Format Section)</span></span>

<span data-ttu-id="01221-104">Indique si l'extrémité du trait est arrondie, carrée ou étendue.</span><span class="sxs-lookup"><span data-stu-id="01221-104">Indicates whether a line has rounded, square, or extended line caps.</span></span>
  
|<span data-ttu-id="01221-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="01221-105">**Value**</span></span>|<span data-ttu-id="01221-106">**Style de l'extrémité du trait**</span><span class="sxs-lookup"><span data-stu-id="01221-106">**Line end style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="01221-107">0</span><span class="sxs-lookup"><span data-stu-id="01221-107">0</span></span>  <br/> |<span data-ttu-id="01221-108">Métro</span><span class="sxs-lookup"><span data-stu-id="01221-108">Rounded</span></span>  <br/> |
|<span data-ttu-id="01221-109">0,1</span><span class="sxs-lookup"><span data-stu-id="01221-109">1</span></span>  <br/> |<span data-ttu-id="01221-110">Square</span><span class="sxs-lookup"><span data-stu-id="01221-110">Square</span></span>  <br/> |
|<span data-ttu-id="01221-111">n°2</span><span class="sxs-lookup"><span data-stu-id="01221-111">2</span></span>  <br/> |<span data-ttu-id="01221-112">Étendue</span><span class="sxs-lookup"><span data-stu-id="01221-112">Extended</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01221-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="01221-113">Remarks</span></span>

<span data-ttu-id="01221-114">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Trait** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Trait**, pointez sur **Flèches**, puis cliquez sur **Autres flèches**).</span><span class="sxs-lookup"><span data-stu-id="01221-114">You can also set the value of this cell in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span>
  
<span data-ttu-id="01221-115">Pour obtenir une référence à la cellule LineCap par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="01221-115">To get a reference to the LineCap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01221-116">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="01221-116">Cell name:</span></span>  <br/> |<span data-ttu-id="01221-117">LineCap</span><span class="sxs-lookup"><span data-stu-id="01221-117">LineCap</span></span>  <br/> |
   
<span data-ttu-id="01221-118">Pour obtenir une référence à la cellule LineCap à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="01221-118">To get a reference to the LineCap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01221-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="01221-119">Section index:</span></span>  <br/> |<span data-ttu-id="01221-120">**Définis**</span><span class="sxs-lookup"><span data-stu-id="01221-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="01221-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="01221-121">Row index:</span></span>  <br/> |<span data-ttu-id="01221-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="01221-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="01221-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="01221-123">Cell index:</span></span>  <br/> |<span data-ttu-id="01221-124">**visLineEndCap**</span><span class="sxs-lookup"><span data-stu-id="01221-124">**visLineEndCap**</span></span> <br/> |
   

