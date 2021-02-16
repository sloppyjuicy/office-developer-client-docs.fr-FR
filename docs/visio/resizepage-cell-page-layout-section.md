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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438091"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="a02e9-103">ResizePage, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="a02e9-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="a02e9-104">Détermine s’il faut agrandir la page pour entourer le  dessin après la disposition  des formes  à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition **de** page, puis cliquez sur Autres **options** de disposition).</span><span class="sxs-lookup"><span data-stu-id="a02e9-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="a02e9-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="a02e9-105">**Value**</span></span>|<span data-ttu-id="a02e9-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="a02e9-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a02e9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a02e9-107">TRUE</span></span>  <br/> | <span data-ttu-id="a02e9-108">La page est agrandie.</span><span class="sxs-lookup"><span data-stu-id="a02e9-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="a02e9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a02e9-109">FALSE</span></span>  <br/> | <span data-ttu-id="a02e9-110">La page n'est pas agrandie.</span><span class="sxs-lookup"><span data-stu-id="a02e9-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a02e9-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="a02e9-111">Remarks</span></span>

<span data-ttu-id="a02e9-112">Pour obtenir une référence à la cellule ResizePage par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="a02e9-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a02e9-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a02e9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a02e9-114">ResizePage</span><span class="sxs-lookup"><span data-stu-id="a02e9-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="a02e9-115">Pour obtenir une référence à la cellule ResizePage à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a02e9-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a02e9-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a02e9-116">Section index:</span></span>  <br/> |<span data-ttu-id="a02e9-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a02e9-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a02e9-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a02e9-118">Row index:</span></span>  <br/> |<span data-ttu-id="a02e9-119">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a02e9-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="a02e9-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a02e9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a02e9-121">**visPLOResizePage**</span><span class="sxs-lookup"><span data-stu-id="a02e9-121">**visPLOResizePage**</span></span> <br/> |
   

