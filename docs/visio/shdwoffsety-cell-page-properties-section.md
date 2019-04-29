---
title: ShdwOffsetY, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: Détermine, en unités de page, la distance du décalage vertical entre l'ombre d'une forme et la forme.
ms.openlocfilehash: be7ec4cccd53cc9d74811e2e45122c8bc29497d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438140"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="7f640-103">ShdwOffsetY, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="7f640-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="7f640-104">Détermine, en unités de page, la distance du décalage vertical entre l'ombre d'une forme et la forme.</span><span class="sxs-lookup"><span data-stu-id="7f640-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f640-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f640-105">Remarks</span></span>

<span data-ttu-id="7f640-p101">Cette valeur est définie dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**). Elle est indépendante de l’échelle du dessin. Si le dessin est mis à l’échelle, le décalage de l’ombre reste le même.</span><span class="sxs-lookup"><span data-stu-id="7f640-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="7f640-109">Pour obtenir une référence à la cellule ShdwOffsetY par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7f640-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7f640-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7f640-110">Cell name:</span></span>  <br/> | <span data-ttu-id="7f640-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="7f640-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="7f640-112">Pour obtenir une référence à la cellule ShdwOffsetY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7f640-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7f640-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7f640-113">Section index:</span></span>  <br/> |<span data-ttu-id="7f640-114">**Définis**</span><span class="sxs-lookup"><span data-stu-id="7f640-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7f640-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7f640-115">Row index:</span></span>  <br/> |<span data-ttu-id="7f640-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="7f640-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="7f640-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7f640-117">Cell index:</span></span>  <br/> |<span data-ttu-id="7f640-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="7f640-118">**visPageShdwOffsetY**</span></span> <br/> |
   

