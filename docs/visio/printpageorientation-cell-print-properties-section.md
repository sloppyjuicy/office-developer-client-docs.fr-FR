---
title: PrintPageOrientation, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033795
localization_priority: Normal
ms.assetid: f8354d0d-0ce2-fb33-ddf7-611a2c24a8be
description: Détermine si la page est imprimée en orientation portrait ou paysage.
ms.openlocfilehash: f7e73bea5120d878a1b2dbf553a66b349d247fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434864"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="aab7d-103">PrintPageOrientation, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="aab7d-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="aab7d-104">Détermine si la page est imprimée en orientation portrait ou paysage.</span><span class="sxs-lookup"><span data-stu-id="aab7d-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="aab7d-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="aab7d-105">**Value**</span></span>|<span data-ttu-id="aab7d-106">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="aab7d-106">**Orientation**</span></span>|<span data-ttu-id="aab7d-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="aab7d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="aab7d-108">0</span><span class="sxs-lookup"><span data-stu-id="aab7d-108">0</span></span>  <br/> | <span data-ttu-id="aab7d-109">Identique au papier de l'imprimante</span><span class="sxs-lookup"><span data-stu-id="aab7d-109">Same as printer</span></span>  <br/> |<span data-ttu-id="aab7d-110">**visPPOSameAsPrinter**</span><span class="sxs-lookup"><span data-stu-id="aab7d-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="aab7d-111">1 </span><span class="sxs-lookup"><span data-stu-id="aab7d-111">1</span></span>  <br/> | <span data-ttu-id="aab7d-112">Portrait</span><span class="sxs-lookup"><span data-stu-id="aab7d-112">Portrait</span></span>  <br/> |<span data-ttu-id="aab7d-113">**visPPOPortrait**</span><span class="sxs-lookup"><span data-stu-id="aab7d-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="aab7d-114">2 </span><span class="sxs-lookup"><span data-stu-id="aab7d-114">2</span></span>  <br/> |<span data-ttu-id="aab7d-115">Paysage</span><span class="sxs-lookup"><span data-stu-id="aab7d-115">Landscape</span></span>  <br/> |<span data-ttu-id="aab7d-116">**visPPOLandscape**</span><span class="sxs-lookup"><span data-stu-id="aab7d-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aab7d-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="aab7d-117">Remarks</span></span>

<span data-ttu-id="aab7d-118">Lorsque vous insérez de nouvelles pages dans un document, ce paramètre est par défaut le paramètre de la page active.</span><span class="sxs-lookup"><span data-stu-id="aab7d-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="aab7d-119">Pour obtenir une référence à la cellule PrintPageOrientation par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="aab7d-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aab7d-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="aab7d-120">Cell name:</span></span>  <br/> | <span data-ttu-id="aab7d-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="aab7d-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="aab7d-122">Pour obtenir une référence à la cellule PrintPageOrientation à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="aab7d-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aab7d-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="aab7d-123">Section index:</span></span>  <br/> |<span data-ttu-id="aab7d-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aab7d-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="aab7d-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="aab7d-125">Row index:</span></span>  <br/> |<span data-ttu-id="aab7d-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="aab7d-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="aab7d-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="aab7d-127">Cell index:</span></span>  <br/> |<span data-ttu-id="aab7d-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="aab7d-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

