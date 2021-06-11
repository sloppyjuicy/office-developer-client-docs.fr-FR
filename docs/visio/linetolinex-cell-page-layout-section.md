---
title: LineToLineX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm565
localization_priority: Normal
ms.assetid: f6b461fe-56ac-4c0e-31cd-6b3c1075db6e
description: Définit l'écart horizontal entre tous les connecteurs de la page de dessin.
ms.openlocfilehash: f3dbf43c737fef1fa1156fb4dc8d0f23449328c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416327"
---
# <a name="linetolinex-cell-page-layout-section"></a><span data-ttu-id="7b359-103">LineToLineX, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="7b359-103">LineToLineX Cell (Page Layout Section)</span></span>

<span data-ttu-id="7b359-104">Définit l'écart horizontal entre tous les connecteurs de la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="7b359-104">Determines the horizontal clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b359-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="7b359-105">Remarks</span></span>

<span data-ttu-id="7b359-p101">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Disposition et positionnement** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, cliquez sur **Disposition et positionnement**, puis sur **Espacement**).</span><span class="sxs-lookup"><span data-stu-id="7b359-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="7b359-108">Pour obtenir une référence à la cellule LineToLineX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7b359-108">To get a reference to the LineToLineX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b359-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7b359-109">Cell name:</span></span>  <br/> |<span data-ttu-id="7b359-110">LineToLineX</span><span class="sxs-lookup"><span data-stu-id="7b359-110">LineToLineX</span></span>  <br/> |
   
<span data-ttu-id="7b359-111">Pour obtenir une référence à la cellule LineToLineX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7b359-111">To get a reference to the LineToLineX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b359-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7b359-112">Section index:</span></span>  <br/> |<span data-ttu-id="7b359-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7b359-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7b359-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7b359-114">Row index:</span></span>  <br/> |<span data-ttu-id="7b359-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="7b359-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="7b359-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7b359-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7b359-117">**visPLOLineToLineX**</span><span class="sxs-lookup"><span data-stu-id="7b359-117">**visPLOLineToLineX**</span></span> <br/> |
   

