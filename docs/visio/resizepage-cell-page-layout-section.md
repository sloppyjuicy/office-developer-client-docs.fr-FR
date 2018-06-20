---
title: ResizePage, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Détermine si la page pour inclure le dessin après la disposition des formes à l’aide de la boîte de dialogue Configurer la disposition est agrandie (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: fab37ee4561ba82ea1f314ad595e513253478b30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789476"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="edbb6-103">ResizePage, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="edbb6-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="edbb6-104">Détermine si la page pour inclure le dessin après la disposition des formes à l’aide de la boîte de dialogue **Configurer la disposition** est agrandie (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en** Page, puis cliquez sur **plus de mise en page Options de**).</span><span class="sxs-lookup"><span data-stu-id="edbb6-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="edbb6-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="edbb6-105">**Value**</span></span>|<span data-ttu-id="edbb6-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="edbb6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="edbb6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="edbb6-107">TRUE</span></span>  <br/> | <span data-ttu-id="edbb6-108">La page est agrandie.</span><span class="sxs-lookup"><span data-stu-id="edbb6-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="edbb6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="edbb6-109">FALSE</span></span>  <br/> | <span data-ttu-id="edbb6-110">La page n'est pas agrandie.</span><span class="sxs-lookup"><span data-stu-id="edbb6-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edbb6-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="edbb6-111">Remarks</span></span>

<span data-ttu-id="edbb6-112">Pour obtenir une référence à la cellule ResizePage par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="edbb6-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="edbb6-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="edbb6-113">Cell name:</span></span>  <br/> | <span data-ttu-id="edbb6-114">ResizePage</span><span class="sxs-lookup"><span data-stu-id="edbb6-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="edbb6-115">Pour obtenir une référence à la cellule ResizePage par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="edbb6-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="edbb6-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="edbb6-116">Section index:</span></span>  <br/> |<span data-ttu-id="edbb6-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="edbb6-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="edbb6-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="edbb6-118">Row index:</span></span>  <br/> |<span data-ttu-id="edbb6-119">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="edbb6-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="edbb6-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="edbb6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="edbb6-121">**visPLOResizePage**</span><span class="sxs-lookup"><span data-stu-id="edbb6-121">**visPLOResizePage**</span></span> <br/> |
   

