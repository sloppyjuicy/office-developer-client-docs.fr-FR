---
title: OnPage, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Indique si le dessin est imprimé sur un nombre spécifique de page d'impression.
ms.openlocfilehash: 5b695ccf6fa2364809e2f5124b9f55ea6aab50e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789182"
---
# <a name="onpage-cell-print-properties-section"></a><span data-ttu-id="d947a-103">OnPage, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="d947a-103">OnPage Cell (Print Properties Section)</span></span>

<span data-ttu-id="d947a-104">Indique si le dessin est imprimé sur un nombre spécifique de page d'impression.</span><span class="sxs-lookup"><span data-stu-id="d947a-104">Indicates whether the drawing is printed on a specific number of printer pages.</span></span> 
  
|<span data-ttu-id="d947a-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="d947a-105">**Value**</span></span>|<span data-ttu-id="d947a-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="d947a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d947a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d947a-107">TRUE</span></span>  <br/> |<span data-ttu-id="d947a-108">Ajuste la page de dessin sur un nombre défini de pages d’impression.</span><span class="sxs-lookup"><span data-stu-id="d947a-108">Fit the drawing page to a defined number of printer pages.</span></span>  <br/> |
|<span data-ttu-id="d947a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d947a-109">FALSE</span></span>  <br/> |<span data-ttu-id="d947a-110">N'ajuste pas la page de dessin sur un nombre défini de pages d'impression (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="d947a-110">Do not fit the drawing page to a defined number of printer pages (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d947a-111">Note</span><span class="sxs-lookup"><span data-stu-id="d947a-111">Remarks</span></span>

<span data-ttu-id="d947a-p101">Si la cellule OnPage est définie sur TRUE, Microsoft Visio utilise les cellules PagesX et PagesY pour déterminer le nombre de pages d’impression sur lesquelles ajuster le dessin. Les valeurs des cellules ScaleX et ScaleY sont ignorées. Ce paramètre peut être considéré comme un paramètre de « mise à l’échelle automatique ».</span><span class="sxs-lookup"><span data-stu-id="d947a-p101">If the OnPage cell is set to TRUE, Microsoft Visio uses the PagesX and PagesY cells to determine the number of printer pages on which to fit the drawing. Values in the ScaleX and ScaleY cells are ignored. This can be considered an "autoscale" setting.</span></span>
  
<span data-ttu-id="d947a-115">Cette valeur correspond à l’option **Ajuster** sur l’onglet **Configuration de l’impression** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ).</span><span class="sxs-lookup"><span data-stu-id="d947a-115">This value corresponds to the **Fit to** option on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) .</span></span> 
  
<span data-ttu-id="d947a-116">Pour obtenir une référence à la cellule OnPage par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="d947a-116">To get a reference to the OnPage cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d947a-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d947a-117">Cell name:</span></span>  <br/> |<span data-ttu-id="d947a-118">OnPage</span><span class="sxs-lookup"><span data-stu-id="d947a-118">OnPage</span></span>  <br/> |
   
<span data-ttu-id="d947a-119">Pour obtenir une référence à la cellule OnPage par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d947a-119">To get a reference to the OnPage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d947a-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d947a-120">Section index:</span></span>  <br/> |<span data-ttu-id="d947a-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d947a-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d947a-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d947a-122">Row index:</span></span>  <br/> |<span data-ttu-id="d947a-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="d947a-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="d947a-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d947a-124">Cell index:</span></span>  <br/> |<span data-ttu-id="d947a-125">**visPrintPropertiesOnPage**</span><span class="sxs-lookup"><span data-stu-id="d947a-125">**visPrintPropertiesOnPage**</span></span> <br/> |
   

