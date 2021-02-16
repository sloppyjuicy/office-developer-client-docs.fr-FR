---
title: ShdwOffsetX, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Détermine, en unités de page, la distance du décalage horizontal entre l'ombre d'une forme et la forme.
ms.openlocfilehash: fbc7d37fc8ba45f3219af6a4350301102954f23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431651"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a><span data-ttu-id="8514d-103">ShdwOffsetX, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="8514d-103">ShdwOffsetX Cell (Page Properties Section)</span></span>

<span data-ttu-id="8514d-104">Détermine, en unités de page, la distance du décalage horizontal entre l'ombre d'une forme et la forme.</span><span class="sxs-lookup"><span data-stu-id="8514d-104">Determines the distance in page units that a shape's drop shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8514d-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="8514d-105">Remarks</span></span>

<span data-ttu-id="8514d-p101">Cette valeur est définie dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**). Elle est indépendante de l’échelle du dessin. Si le dessin est mis à l’échelle, le décalage de l’ombre reste le même.</span><span class="sxs-lookup"><span data-stu-id="8514d-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="8514d-109">Pour obtenir une référence à la cellule ShdwOffsetX par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="8514d-109">To get a reference to the ShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8514d-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8514d-110">Cell name:</span></span>  <br/> | <span data-ttu-id="8514d-111">ShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="8514d-111">ShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="8514d-112">Pour obtenir une référence à la cellule ShdwOffsetX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8514d-112">To get a reference to the ShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8514d-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8514d-113">Section index:</span></span>  <br/> |<span data-ttu-id="8514d-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8514d-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8514d-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8514d-115">Row index:</span></span>  <br/> |<span data-ttu-id="8514d-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="8514d-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="8514d-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8514d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="8514d-118">**visPageShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="8514d-118">**visPageShdwOffsetX**</span></span> <br/> |
   

