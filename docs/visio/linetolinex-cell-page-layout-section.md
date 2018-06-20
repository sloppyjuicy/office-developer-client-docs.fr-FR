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
ms.openlocfilehash: aa6476eab9d5bcf7aab12235fd23f0f5675d6ad5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788955"
---
# <a name="linetolinex-cell-page-layout-section"></a><span data-ttu-id="bf390-103">LineToLineX, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="bf390-103">LineToLineX Cell (Page Layout Section)</span></span>

<span data-ttu-id="bf390-104">Définit l'écart horizontal entre tous les connecteurs de la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="bf390-104">Determines the horizontal clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf390-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="bf390-105">Remarks</span></span>

<span data-ttu-id="bf390-106">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **disposition et positionnement** .</span><span class="sxs-lookup"><span data-stu-id="bf390-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="bf390-107">(Sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , cliquez sur **disposition et positionnement**, puis cliquez sur **espacement**.)</span><span class="sxs-lookup"><span data-stu-id="bf390-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="bf390-108">Pour obtenir une référence à la cellule LineToLineX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="bf390-108">To get a reference to the LineToLineX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf390-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bf390-109">Cell name:</span></span>  <br/> |<span data-ttu-id="bf390-110">LineToLineX</span><span class="sxs-lookup"><span data-stu-id="bf390-110">LineToLineX</span></span>  <br/> |
   
<span data-ttu-id="bf390-111">Pour obtenir une référence à la cellule LineToLineX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bf390-111">To get a reference to the LineToLineX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf390-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bf390-112">Section index:</span></span>  <br/> |<span data-ttu-id="bf390-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bf390-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bf390-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bf390-114">Row index:</span></span>  <br/> |<span data-ttu-id="bf390-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="bf390-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="bf390-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bf390-116">Cell index:</span></span>  <br/> |<span data-ttu-id="bf390-117">**visPLOLineToLineX**</span><span class="sxs-lookup"><span data-stu-id="bf390-117">**visPLOLineToLineX**</span></span> <br/> |
   

