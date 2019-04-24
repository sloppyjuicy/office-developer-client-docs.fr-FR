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
description: Détermine si la page doit être agrandie pour inclure le dessin après la disposition automatique des formes à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de page, puis cliquez sur Autres options de disposition).
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326823"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="04710-103">ResizePage, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="04710-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="04710-104">Détermine si la page doit être agrandie pour encadrer le dessin après la disposition des formes à l'aide de la boîte de dialogue **configurer la disposition** (sous l'onglet **création** , dans le groupe **disposition** , cliquez sur **nouvelle disposition** de page, puis cliquez sur **autres dispositions Options**).</span><span class="sxs-lookup"><span data-stu-id="04710-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="04710-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="04710-105">**Value**</span></span>|<span data-ttu-id="04710-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="04710-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="04710-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="04710-107">TRUE</span></span>  <br/> | <span data-ttu-id="04710-108">La page est agrandie.</span><span class="sxs-lookup"><span data-stu-id="04710-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="04710-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="04710-109">FALSE</span></span>  <br/> | <span data-ttu-id="04710-110">La page n'est pas agrandie.</span><span class="sxs-lookup"><span data-stu-id="04710-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04710-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="04710-111">Remarks</span></span>

<span data-ttu-id="04710-112">Pour obtenir une référence à la cellule ResizePage par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="04710-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04710-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="04710-113">Cell name:</span></span>  <br/> | <span data-ttu-id="04710-114">ResizePage</span><span class="sxs-lookup"><span data-stu-id="04710-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="04710-115">Pour obtenir une référence à la cellule ResizePage à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="04710-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04710-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="04710-116">Section index:</span></span>  <br/> |<span data-ttu-id="04710-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="04710-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="04710-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="04710-118">Row index:</span></span>  <br/> |<span data-ttu-id="04710-119">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="04710-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="04710-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="04710-120">Cell index:</span></span>  <br/> |<span data-ttu-id="04710-121">**visPLOResizePage**</span><span class="sxs-lookup"><span data-stu-id="04710-121">**visPLOResizePage**</span></span> <br/> |
   

