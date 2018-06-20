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
ms.openlocfilehash: 75f7e8150711421138a01175be34003d124e88ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788964"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="483f5-103">LineToNodeX, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="483f5-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="483f5-104">Définit l'écart horizontal entre tous les connecteurs et les formes de la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="483f5-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="483f5-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="483f5-105">Remarks</span></span>

<span data-ttu-id="483f5-106">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **disposition et positionnement** .</span><span class="sxs-lookup"><span data-stu-id="483f5-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="483f5-107">(Sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , cliquez sur **disposition et positionnement**, puis cliquez sur **espacement**.)</span><span class="sxs-lookup"><span data-stu-id="483f5-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="483f5-108">Pour obtenir une référence à la cellule LineToNodeY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="483f5-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="483f5-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="483f5-109">Cell name:</span></span>  <br/> |<span data-ttu-id="483f5-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="483f5-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="483f5-111">Pour obtenir une référence à la cellule LineToNodeX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="483f5-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="483f5-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="483f5-112">Section index:</span></span>  <br/> |<span data-ttu-id="483f5-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="483f5-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="483f5-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="483f5-114">Row index:</span></span>  <br/> |<span data-ttu-id="483f5-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="483f5-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="483f5-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="483f5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="483f5-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="483f5-117">**visPLOLineToNodeX**</span></span> <br/> |
   

