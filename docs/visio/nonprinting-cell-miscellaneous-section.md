---
title: NonPrinting, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Active ou désactive l'impression de la forme sélectionnée.
ms.openlocfilehash: c3e1fc1b2d91fa4808f8ea89c904218c2236f5b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437258"
---
# <a name="nonprinting-cell-miscellaneous-section"></a><span data-ttu-id="ccbb9-103">NonPrinting, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="ccbb9-103">NonPrinting Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="ccbb9-104">Active ou désactive l'impression de la forme sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ccbb9-104">Switches printing on and off for the selected shape.</span></span>
  
|<span data-ttu-id="ccbb9-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ccbb9-105">**Value**</span></span>|<span data-ttu-id="ccbb9-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="ccbb9-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ccbb9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ccbb9-107">TRUE</span></span>  <br/> | <span data-ttu-id="ccbb9-108">L'impression est désactivée mais la forme est affichée dans la fenêtre de dessin.</span><span class="sxs-lookup"><span data-stu-id="ccbb9-108">Printing disabled, but the shape will be displayed in the drawing window.</span></span>  <br/> |
| <span data-ttu-id="ccbb9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ccbb9-109">FALSE</span></span>  <br/> | <span data-ttu-id="ccbb9-110">L'impression est activée.</span><span class="sxs-lookup"><span data-stu-id="ccbb9-110">Printing enabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ccbb9-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="ccbb9-111">Remarks</span></span>

<span data-ttu-id="ccbb9-112">Pour imprimer un repère, sélectionnez-le, puis affectez la valeur FALSE à la cellule NonPrinting.</span><span class="sxs-lookup"><span data-stu-id="ccbb9-112">You can print a guide by selecting it, and then setting the value of its NonPrinting cell to FALSE.</span></span>
  
<span data-ttu-id="ccbb9-113">Pour obtenir une référence à la cellule NonPrinting par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ccbb9-113">To get a reference to the NonPrinting cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ccbb9-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ccbb9-114">Cell name:</span></span>  <br/> | <span data-ttu-id="ccbb9-115">Non imprimables</span><span class="sxs-lookup"><span data-stu-id="ccbb9-115">NonPrinting</span></span>  <br/> |
   
<span data-ttu-id="ccbb9-116">Pour obtenir une référence à la cellule NonPrinting à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ccbb9-116">To get a reference to the NonPrinting cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ccbb9-117">Index de la section  :</span><span class="sxs-lookup"><span data-stu-id="ccbb9-117">Section index:</span></span>  <br/> |<span data-ttu-id="ccbb9-118">**Définis**</span><span class="sxs-lookup"><span data-stu-id="ccbb9-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ccbb9-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ccbb9-119">Row index:</span></span>  <br/> |<span data-ttu-id="ccbb9-120">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="ccbb9-120">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="ccbb9-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ccbb9-121">Cell index:</span></span>  <br/> |<span data-ttu-id="ccbb9-122">**visNonPrinting**</span><span class="sxs-lookup"><span data-stu-id="ccbb9-122">**visNonPrinting**</span></span> <br/> |
   

