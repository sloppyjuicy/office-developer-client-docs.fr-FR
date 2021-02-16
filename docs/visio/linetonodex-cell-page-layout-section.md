---
title: LineToNodeX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm575
localization_priority: Normal
ms.assetid: 9d58e23e-b411-c5c1-b785-5014488d42c8
description: Définit l'écart horizontal entre tous les connecteurs et les formes de la page de dessin.
ms.openlocfilehash: c5a27edb25ce7b1449ad6e2988027b474bd79fdb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439708"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="e68ac-103">LineToNodeX, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="e68ac-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="e68ac-104">Définit l'écart horizontal entre tous les connecteurs et les formes de la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="e68ac-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e68ac-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="e68ac-105">Remarks</span></span>

<span data-ttu-id="e68ac-p101">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Disposition et positionnement** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, cliquez sur **Disposition et positionnement**, puis sur **Espacement**).</span><span class="sxs-lookup"><span data-stu-id="e68ac-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="e68ac-108">Pour obtenir une référence à la cellule LineToNodeY par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="e68ac-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e68ac-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e68ac-109">Cell name:</span></span>  <br/> |<span data-ttu-id="e68ac-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="e68ac-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="e68ac-111">Pour obtenir une référence à la cellule LineToNodeX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e68ac-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e68ac-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e68ac-112">Section index:</span></span>  <br/> |<span data-ttu-id="e68ac-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e68ac-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e68ac-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e68ac-114">Row index:</span></span>  <br/> |<span data-ttu-id="e68ac-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e68ac-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="e68ac-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e68ac-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e68ac-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="e68ac-117">**visPLOLineToNodeX**</span></span> <br/> |
   

