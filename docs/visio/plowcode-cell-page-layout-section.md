---
title: PlowCode, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Détermine si les formes positionnables se déplacent lorsque vous déposez une forme positionnable à côté d'une autre forme positionnable sur une page de dessin.
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420352"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="bb953-103">PlowCode, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="bb953-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="bb953-104">Détermine si les formes positionnables se déplacent lorsque vous déposez une forme positionnable à côté d'une autre forme positionnable sur une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="bb953-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="bb953-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="bb953-105">**Value**</span></span>|<span data-ttu-id="bb953-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="bb953-106">**Description**</span></span>|<span data-ttu-id="bb953-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="bb953-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb953-108">0</span><span class="sxs-lookup"><span data-stu-id="bb953-108">0</span></span>  <br/> |<span data-ttu-id="bb953-109">Ne pas déplacer les formes</span><span class="sxs-lookup"><span data-stu-id="bb953-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="bb953-110">**visPLOPlowNone**</span><span class="sxs-lookup"><span data-stu-id="bb953-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="bb953-111">1 </span><span class="sxs-lookup"><span data-stu-id="bb953-111">1</span></span>  <br/> |<span data-ttu-id="bb953-112">Déplacer les formes</span><span class="sxs-lookup"><span data-stu-id="bb953-112">Move shapes</span></span>  <br/> |<span data-ttu-id="bb953-113">**visPLOPlowAll**</span><span class="sxs-lookup"><span data-stu-id="bb953-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb953-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb953-114">Remarks</span></span>

<span data-ttu-id="bb953-115">Vous pouvez également définir la valeur  de cette cellule sous l’onglet Mise en page et routage dans  la boîte de dialogue Mise en **page** (sous l’onglet Création, cliquez sur la flèche Mise en **page)** à l’aide de la case à cocher Déplacer d’autres formes dans la zone de dépôt. </span><span class="sxs-lookup"><span data-stu-id="bb953-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="bb953-116">Pour obtenir une référence à la cellule PlowCode par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="bb953-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb953-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bb953-117">Cell name:</span></span>  <br/> |<span data-ttu-id="bb953-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="bb953-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="bb953-119">Pour obtenir une référence à la cellule PlowCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bb953-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb953-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bb953-120">Section index:</span></span>  <br/> |<span data-ttu-id="bb953-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bb953-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bb953-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bb953-122">Row index:</span></span>  <br/> |<span data-ttu-id="bb953-123">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="bb953-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="bb953-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bb953-124">Cell index:</span></span>  <br/> |<span data-ttu-id="bb953-125">**visPLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="bb953-125">**visPLOPlowCode**</span></span> <br/> |
   

