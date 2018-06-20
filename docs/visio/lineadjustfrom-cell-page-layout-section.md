---
title: LineAdjustFrom, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Détermine quels connecteurs dynamiques doivent être espacés par l'application s'ils sont positionnés les uns sur les autres.
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788936"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="270c7-103">LineAdjustFrom, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="270c7-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="270c7-104">Détermine quels connecteurs dynamiques doivent être espacés par l'application s'ils sont positionnés les uns sur les autres.</span><span class="sxs-lookup"><span data-stu-id="270c7-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="270c7-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="270c7-105">**Value**</span></span>|<span data-ttu-id="270c7-106">**Ajustement**</span><span class="sxs-lookup"><span data-stu-id="270c7-106">**Adjustment**</span></span>|<span data-ttu-id="270c7-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="270c7-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="270c7-108">0</span><span class="sxs-lookup"><span data-stu-id="270c7-108">0</span></span>  <br/> |<span data-ttu-id="270c7-109">Traits sans relation</span><span class="sxs-lookup"><span data-stu-id="270c7-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="270c7-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="270c7-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="270c7-111">1</span><span class="sxs-lookup"><span data-stu-id="270c7-111">1</span></span>  <br/> |<span data-ttu-id="270c7-112">Tous les traits</span><span class="sxs-lookup"><span data-stu-id="270c7-112">All lines</span></span>  <br/> |<span data-ttu-id="270c7-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="270c7-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="270c7-114">2</span><span class="sxs-lookup"><span data-stu-id="270c7-114">2</span></span>  <br/> |<span data-ttu-id="270c7-115">Aucun trait</span><span class="sxs-lookup"><span data-stu-id="270c7-115">No lines</span></span>  <br/> |<span data-ttu-id="270c7-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="270c7-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="270c7-117">3</span><span class="sxs-lookup"><span data-stu-id="270c7-117">3</span></span>  <br/> |<span data-ttu-id="270c7-118">Style de positionnement par défaut</span><span class="sxs-lookup"><span data-stu-id="270c7-118">Routing style default</span></span>  <br/> |<span data-ttu-id="270c7-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="270c7-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="270c7-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="270c7-120">Remarks</span></span>

<span data-ttu-id="270c7-121">Vous pouvez également définir la valeur de cette cellule sous l’onglet **disposition et positionnement** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , puis cliquez sur **disposition et positionnement**).</span><span class="sxs-lookup"><span data-stu-id="270c7-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="270c7-122">Pour obtenir une référence à la cellule LineAdjustFrom par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="270c7-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="270c7-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="270c7-123">Cell name:</span></span>  <br/> |<span data-ttu-id="270c7-124">LineAdjustFrom</span><span class="sxs-lookup"><span data-stu-id="270c7-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="270c7-125">Pour obtenir une référence à la cellule LineAdjustFrom par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="270c7-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="270c7-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="270c7-126">Section index:</span></span>  <br/> |<span data-ttu-id="270c7-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="270c7-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="270c7-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="270c7-128">Row index:</span></span>  <br/> |<span data-ttu-id="270c7-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="270c7-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="270c7-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="270c7-130">Cell index:</span></span>  <br/> |<span data-ttu-id="270c7-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="270c7-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

