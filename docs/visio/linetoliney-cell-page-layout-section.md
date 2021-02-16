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
ms.openlocfilehash: e98c3e05ffb1739f9b2739ce4e0ee8012afe2266
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428472"
---
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="ee1ad-103">LineToLineY, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="ee1ad-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="ee1ad-104">Définit l'écart vertical entre tous les connecteurs de la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="ee1ad-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee1ad-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee1ad-105">Remarks</span></span>

<span data-ttu-id="ee1ad-p101">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Disposition et positionnement** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**, cliquez sur **Disposition et positionnement**, puis sur **Espacement**).</span><span class="sxs-lookup"><span data-stu-id="ee1ad-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="ee1ad-108">Pour obtenir une référence à la cellule LineToLineY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ee1ad-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee1ad-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ee1ad-109">Cell name:</span></span>  <br/> |<span data-ttu-id="ee1ad-110">LineToLiney</span><span class="sxs-lookup"><span data-stu-id="ee1ad-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="ee1ad-111">Pour obtenir une référence à la cellule LineToLineY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ee1ad-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee1ad-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ee1ad-112">Section index:</span></span>  <br/> |<span data-ttu-id="ee1ad-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ee1ad-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ee1ad-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ee1ad-114">Row index:</span></span>  <br/> |<span data-ttu-id="ee1ad-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="ee1ad-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="ee1ad-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ee1ad-116">Cell index:</span></span>  <br/> |<span data-ttu-id="ee1ad-117">**visPLOLineToLineY**</span><span class="sxs-lookup"><span data-stu-id="ee1ad-117">**visPLOLineToLineY**</span></span> <br/> |
   

