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
ms.openlocfilehash: e180ce679f280cbccbda80b67170f2f26473bd8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789273"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="10c88-103">PlowCode, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="10c88-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="10c88-104">Détermine si les formes positionnables se déplacent lorsque vous déposez une forme positionnable à côté d'une autre forme positionnable sur une page de dessin.</span><span class="sxs-lookup"><span data-stu-id="10c88-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="10c88-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="10c88-105">**Value**</span></span>|<span data-ttu-id="10c88-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="10c88-106">**Description**</span></span>|<span data-ttu-id="10c88-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="10c88-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="10c88-108">0</span><span class="sxs-lookup"><span data-stu-id="10c88-108">0</span></span>  <br/> |<span data-ttu-id="10c88-109">Ne pas déplacer les formes</span><span class="sxs-lookup"><span data-stu-id="10c88-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="10c88-110">**visPLOPlowNone**</span><span class="sxs-lookup"><span data-stu-id="10c88-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="10c88-111">1</span><span class="sxs-lookup"><span data-stu-id="10c88-111">1</span></span>  <br/> |<span data-ttu-id="10c88-112">Déplacer les formes</span><span class="sxs-lookup"><span data-stu-id="10c88-112">Move shapes</span></span>  <br/> |<span data-ttu-id="10c88-113">**visPLOPlowAll**</span><span class="sxs-lookup"><span data-stu-id="10c88-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10c88-114">Note</span><span class="sxs-lookup"><span data-stu-id="10c88-114">Remarks</span></span>

<span data-ttu-id="10c88-115">Vous pouvez également définir la valeur de cette cellule sous l’onglet **disposition et positionnement** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ) à l’aide de la case à cocher **déplacer les autres formes lors de l’insertion** .</span><span class="sxs-lookup"><span data-stu-id="10c88-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="10c88-116">Pour obtenir une référence à la cellule PlowCode par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="10c88-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10c88-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="10c88-117">Cell name:</span></span>  <br/> |<span data-ttu-id="10c88-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="10c88-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="10c88-119">Pour obtenir une référence à la cellule PlowCode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="10c88-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10c88-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="10c88-120">Section index:</span></span>  <br/> |<span data-ttu-id="10c88-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="10c88-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="10c88-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="10c88-122">Row index:</span></span>  <br/> |<span data-ttu-id="10c88-123">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="10c88-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="10c88-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="10c88-124">Cell index:</span></span>  <br/> |<span data-ttu-id="10c88-125">**visPLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="10c88-125">**visPLOPlowCode**</span></span> <br/> |
   

