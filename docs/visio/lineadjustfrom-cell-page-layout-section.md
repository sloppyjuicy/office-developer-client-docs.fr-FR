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
ms.openlocfilehash: 3eb9f5513ee3ce2f5dce96cb47c356bca29a289c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415186"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a><span data-ttu-id="2df68-103">LineAdjustFrom, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="2df68-103">LineAdjustFrom Cell (Page Layout Section)</span></span>

<span data-ttu-id="2df68-104">Détermine quels connecteurs dynamiques doivent être espacés par l'application s'ils sont positionnés les uns sur les autres.</span><span class="sxs-lookup"><span data-stu-id="2df68-104">Determines which dynamic connectors the application spaces apart if they route on top of each other.</span></span>
  
|<span data-ttu-id="2df68-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2df68-105">**Value**</span></span>|<span data-ttu-id="2df68-106">**Ajustement**</span><span class="sxs-lookup"><span data-stu-id="2df68-106">**Adjustment**</span></span>|<span data-ttu-id="2df68-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="2df68-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2df68-108">0</span><span class="sxs-lookup"><span data-stu-id="2df68-108">0</span></span>  <br/> |<span data-ttu-id="2df68-109">Traits sans relation</span><span class="sxs-lookup"><span data-stu-id="2df68-109">Unrelated lines</span></span>  <br/> |<span data-ttu-id="2df68-110">**visPLOLineAdjustFromNotRelated**</span><span class="sxs-lookup"><span data-stu-id="2df68-110">**visPLOLineAdjustFromNotRelated**</span></span> <br/> |
|<span data-ttu-id="2df68-111">0,1</span><span class="sxs-lookup"><span data-stu-id="2df68-111">1</span></span>  <br/> |<span data-ttu-id="2df68-112">Tous les traits</span><span class="sxs-lookup"><span data-stu-id="2df68-112">All lines</span></span>  <br/> |<span data-ttu-id="2df68-113">**visPLOLineAdjustFromAll**</span><span class="sxs-lookup"><span data-stu-id="2df68-113">**visPLOLineAdjustFromAll**</span></span> <br/> |
|<span data-ttu-id="2df68-114">n°2</span><span class="sxs-lookup"><span data-stu-id="2df68-114">2</span></span>  <br/> |<span data-ttu-id="2df68-115">Aucun trait</span><span class="sxs-lookup"><span data-stu-id="2df68-115">No lines</span></span>  <br/> |<span data-ttu-id="2df68-116">**visPLOLineAdjustFromNone**</span><span class="sxs-lookup"><span data-stu-id="2df68-116">**visPLOLineAdjustFromNone**</span></span> <br/> |
|<span data-ttu-id="2df68-117">3</span><span class="sxs-lookup"><span data-stu-id="2df68-117">3</span></span>  <br/> |<span data-ttu-id="2df68-118">Style de positionnement par défaut</span><span class="sxs-lookup"><span data-stu-id="2df68-118">Routing style default</span></span>  <br/> |<span data-ttu-id="2df68-119">**visPLOLineAdjustFromRoutingDefault**</span><span class="sxs-lookup"><span data-stu-id="2df68-119">**visPLOLineAdjustFromRoutingDefault**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2df68-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="2df68-120">Remarks</span></span>

<span data-ttu-id="2df68-121">Vous pouvez également définir la valeur de cette cellule dans l’onglet **Disposition et positionnement** dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, puis cliquez sur **Disposition et positionnement**).</span><span class="sxs-lookup"><span data-stu-id="2df68-121">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="2df68-122">Pour obtenir une référence à la cellule LineAdjustFrom par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="2df68-122">To get a reference to the LineAdjustFrom cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2df68-123">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2df68-123">Cell name:</span></span>  <br/> |<span data-ttu-id="2df68-124">LineAdjustFrom</span><span class="sxs-lookup"><span data-stu-id="2df68-124">LineAdjustFrom</span></span>  <br/> |
   
<span data-ttu-id="2df68-125">Pour obtenir une référence à la cellule LineAdjustFrom à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2df68-125">To get a reference to the LineAdjustFrom cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2df68-126">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2df68-126">Section index:</span></span>  <br/> |<span data-ttu-id="2df68-127">**Définis**</span><span class="sxs-lookup"><span data-stu-id="2df68-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2df68-128">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2df68-128">Row index:</span></span>  <br/> |<span data-ttu-id="2df68-129">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="2df68-129">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="2df68-130">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2df68-130">Cell index:</span></span>  <br/> |<span data-ttu-id="2df68-131">**visPLOLineAdjustFrom**</span><span class="sxs-lookup"><span data-stu-id="2df68-131">**visPLOLineAdjustFrom**</span></span> <br/> |
   

