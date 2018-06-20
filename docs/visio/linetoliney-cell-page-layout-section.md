---
title: LineToLineY, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm570
localization_priority: Normal
ms.assetid: db9a8232-25c5-7087-2ae9-50470d0cf16e
description: Définit l'écart vertical entre tous les connecteurs de la page de dessin.
ms.openlocfilehash: 781d166fe0b81cc2402fde2894cd1d0480a0895f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788960"
---
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="92135-103">LineToLineY, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="92135-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="92135-104">Définit l'écart vertical entre tous les connecteurs de la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="92135-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="92135-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="92135-105">Remarks</span></span>

<span data-ttu-id="92135-106">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **disposition et positionnement** .</span><span class="sxs-lookup"><span data-stu-id="92135-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="92135-107">(Sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , cliquez sur **disposition et positionnement**, puis cliquez sur **espacement**.)</span><span class="sxs-lookup"><span data-stu-id="92135-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="92135-108">Pour obtenir une référence à la cellule LineToLineY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="92135-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92135-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="92135-109">Cell name:</span></span>  <br/> |<span data-ttu-id="92135-110">LineToLineY</span><span class="sxs-lookup"><span data-stu-id="92135-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="92135-111">Pour obtenir une référence à la cellule LineToLineY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="92135-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92135-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="92135-112">Section index:</span></span>  <br/> |<span data-ttu-id="92135-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="92135-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="92135-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="92135-114">Row index:</span></span>  <br/> |<span data-ttu-id="92135-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="92135-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="92135-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="92135-116">Cell index:</span></span>  <br/> |<span data-ttu-id="92135-117">**visPLOLineToLineY**</span><span class="sxs-lookup"><span data-stu-id="92135-117">**visPLOLineToLineY**</span></span> <br/> |
   

