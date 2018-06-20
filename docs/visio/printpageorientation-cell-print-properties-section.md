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
ms.openlocfilehash: 2adc7dadcb3702e6c5307bb569b2ae1df7aee54e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789361"
---
# <a name="printpageorientation-cell-print-properties-section"></a><span data-ttu-id="2cc9c-103">PrintPageOrientation, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="2cc9c-103">PrintPageOrientation Cell (Print Properties Section)</span></span>

<span data-ttu-id="2cc9c-104">Détermine si la page est imprimée en orientation portrait ou paysage.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-104">Determines whether the page prints using portrait or landscape orientation.</span></span>
  
|<span data-ttu-id="2cc9c-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2cc9c-105">**Value**</span></span>|<span data-ttu-id="2cc9c-106">**Orientation**</span><span class="sxs-lookup"><span data-stu-id="2cc9c-106">**Orientation**</span></span>|<span data-ttu-id="2cc9c-107">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="2cc9c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2cc9c-108">0</span><span class="sxs-lookup"><span data-stu-id="2cc9c-108">0</span></span>  <br/> | <span data-ttu-id="2cc9c-109">Identique au papier de l'imprimante</span><span class="sxs-lookup"><span data-stu-id="2cc9c-109">Same as printer</span></span>  <br/> |<span data-ttu-id="2cc9c-110">**visPPOSameAsPrinter**</span><span class="sxs-lookup"><span data-stu-id="2cc9c-110">**visPPOSameAsPrinter**</span></span> <br/> |
| <span data-ttu-id="2cc9c-111">1</span><span class="sxs-lookup"><span data-stu-id="2cc9c-111">1</span></span>  <br/> | <span data-ttu-id="2cc9c-112">Portrait</span><span class="sxs-lookup"><span data-stu-id="2cc9c-112">Portrait</span></span>  <br/> |<span data-ttu-id="2cc9c-113">**visPPOPortrait**</span><span class="sxs-lookup"><span data-stu-id="2cc9c-113">**visPPOPortrait**</span></span> <br/> |
|<span data-ttu-id="2cc9c-114">2</span><span class="sxs-lookup"><span data-stu-id="2cc9c-114">2</span></span>  <br/> |<span data-ttu-id="2cc9c-115">Paysage</span><span class="sxs-lookup"><span data-stu-id="2cc9c-115">Landscape</span></span>  <br/> |<span data-ttu-id="2cc9c-116">**visPPOLandscape**</span><span class="sxs-lookup"><span data-stu-id="2cc9c-116">**visPPOLandscape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cc9c-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="2cc9c-117">Remarks</span></span>

<span data-ttu-id="2cc9c-118">Lorsque vous insérez de nouvelles pages dans un document, ce paramètre par défaut pour le paramètre dans la page active.</span><span class="sxs-lookup"><span data-stu-id="2cc9c-118">When you insert new pages in a document, this setting defaults to the setting in the active page.</span></span>
  
<span data-ttu-id="2cc9c-119">Pour obtenir une référence à la cellule PrintPageOrientation par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="2cc9c-119">To get a reference to the PrintPageOrientation cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2cc9c-120">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2cc9c-120">Cell name:</span></span>  <br/> | <span data-ttu-id="2cc9c-121">PrintPageOrientation</span><span class="sxs-lookup"><span data-stu-id="2cc9c-121">PrintPageOrientation</span></span>  <br/> |
   
<span data-ttu-id="2cc9c-122">Pour obtenir une référence à la cellule PrintPageOrientation par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2cc9c-122">To get a reference to the PrintPageOrientation cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2cc9c-123">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2cc9c-123">Section index:</span></span>  <br/> |<span data-ttu-id="2cc9c-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2cc9c-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2cc9c-125">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2cc9c-125">Row index:</span></span>  <br/> |<span data-ttu-id="2cc9c-126">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="2cc9c-126">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="2cc9c-127">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2cc9c-127">Cell index:</span></span>  <br/> |<span data-ttu-id="2cc9c-128">**visPrintPropertiesPageOrientation**</span><span class="sxs-lookup"><span data-stu-id="2cc9c-128">**visPrintPropertiesPageOrientation**</span></span> <br/> |
   

