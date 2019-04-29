---
title: OutputFormat, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Détermine le format de sortie d'un dessin. Les pages de dessin sont généralement mises en forme pour l'impression (par défaut), mais vous pouvez choisir d'autres formats de sortie.
ms.openlocfilehash: 09fa34095772936ab1c6a3025ed1884a533f55e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413884"
---
# <a name="outputformat-cell-document-properties-section"></a><span data-ttu-id="ad83a-104">OutputFormat, cellule (section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="ad83a-104">OutputFormat Cell (Document Properties Section)</span></span>

<span data-ttu-id="ad83a-105">Détermine le format de sortie d'un dessin.</span><span class="sxs-lookup"><span data-stu-id="ad83a-105">Determines the output format for a drawing.</span></span> <span data-ttu-id="ad83a-106">Les pages de dessin sont généralement mises en forme pour l'impression (par défaut), mais vous pouvez choisir d'autres formats de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad83a-106">Drawing pages are usually formatted for printing (default); however, you can choose other output formats.</span></span>
  
|<span data-ttu-id="ad83a-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ad83a-107">**Value**</span></span>|<span data-ttu-id="ad83a-108">**Format de sortie**</span><span class="sxs-lookup"><span data-stu-id="ad83a-108">**Output format**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ad83a-109">0</span><span class="sxs-lookup"><span data-stu-id="ad83a-109">0</span></span>  <br/> | <span data-ttu-id="ad83a-110">Impression (par défaut)</span><span class="sxs-lookup"><span data-stu-id="ad83a-110">Printing (default)</span></span>  <br/> |
| <span data-ttu-id="ad83a-111">0,1</span><span class="sxs-lookup"><span data-stu-id="ad83a-111">1</span></span>  <br/> | <span data-ttu-id="ad83a-112">Diaporama PowerPoint</span><span class="sxs-lookup"><span data-stu-id="ad83a-112">PowerPoint slide show</span></span>  <br/> |
| <span data-ttu-id="ad83a-113">n°2</span><span class="sxs-lookup"><span data-stu-id="ad83a-113">2</span></span>  <br/> | <span data-ttu-id="ad83a-114">Sortie HTML ou GIF</span><span class="sxs-lookup"><span data-stu-id="ad83a-114">HTML or GIF output</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad83a-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="ad83a-115">Remarks</span></span>

<span data-ttu-id="ad83a-116">Pour obtenir une référence à la cellule OutputFormat par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ad83a-116">To get a reference to the OutputFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad83a-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ad83a-117">Cell name:</span></span>  <br/> | <span data-ttu-id="ad83a-118">OutputFormat</span><span class="sxs-lookup"><span data-stu-id="ad83a-118">OutputFormat</span></span>  <br/> |
   
<span data-ttu-id="ad83a-119">Pour obtenir une référence à la cellule OutputFormat à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ad83a-119">To get a reference to the OutputFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ad83a-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ad83a-120">Section index:</span></span>  <br/> |<span data-ttu-id="ad83a-121">**Définis**</span><span class="sxs-lookup"><span data-stu-id="ad83a-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ad83a-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ad83a-122">Row index:</span></span>  <br/> |<span data-ttu-id="ad83a-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="ad83a-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="ad83a-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ad83a-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ad83a-125">**visDocOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="ad83a-125">**visDocOutputFormat**</span></span> <br/> |
   

