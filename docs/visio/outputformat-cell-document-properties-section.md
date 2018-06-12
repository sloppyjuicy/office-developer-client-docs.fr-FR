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
ms.openlocfilehash: 7103fa5c2bc721add3496b7a497989d6632d58f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789190"
---
# <a name="outputformat-cell-document-properties-section"></a><span data-ttu-id="ac3be-104">OutputFormat, cellule (section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="ac3be-104">OutputFormat Cell (Document Properties Section)</span></span>

<span data-ttu-id="ac3be-p102">Détermine le format de sortie d'un dessin. Les pages de dessin sont généralement mises en forme pour l'impression (par défaut), mais vous pouvez choisir d'autres formats de sortie.</span><span class="sxs-lookup"><span data-stu-id="ac3be-p102">Determines the output format for a drawing. Drawing pages are usually formatted for printing (default); however, you can choose other output formats.</span></span>
  
|<span data-ttu-id="ac3be-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ac3be-107">**Value**</span></span>|<span data-ttu-id="ac3be-108">**Format de sortie**</span><span class="sxs-lookup"><span data-stu-id="ac3be-108">**Output format**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ac3be-109">0</span><span class="sxs-lookup"><span data-stu-id="ac3be-109">0</span></span>  <br/> | <span data-ttu-id="ac3be-110">Impression (par défaut)</span><span class="sxs-lookup"><span data-stu-id="ac3be-110">Printing (default)</span></span>  <br/> |
| <span data-ttu-id="ac3be-111">1</span><span class="sxs-lookup"><span data-stu-id="ac3be-111">1</span></span>  <br/> | <span data-ttu-id="ac3be-112">Diaporama PowerPoint</span><span class="sxs-lookup"><span data-stu-id="ac3be-112">PowerPoint slide show</span></span>  <br/> |
| <span data-ttu-id="ac3be-113">2</span><span class="sxs-lookup"><span data-stu-id="ac3be-113">2</span></span>  <br/> | <span data-ttu-id="ac3be-114">Sortie HTML ou GIF</span><span class="sxs-lookup"><span data-stu-id="ac3be-114">HTML or GIF output</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac3be-115">Note</span><span class="sxs-lookup"><span data-stu-id="ac3be-115">Remarks</span></span>

<span data-ttu-id="ac3be-116">Pour obtenir une référence à la cellule OutputFormat par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="ac3be-116">To get a reference to the OutputFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ac3be-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ac3be-117">Cell name:</span></span>  <br/> | <span data-ttu-id="ac3be-118">OutputFormat</span><span class="sxs-lookup"><span data-stu-id="ac3be-118">OutputFormat</span></span>  <br/> |
   
<span data-ttu-id="ac3be-119">Pour obtenir une référence à la cellule OutputFormat par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ac3be-119">To get a reference to the OutputFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ac3be-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ac3be-120">Section index:</span></span>  <br/> |<span data-ttu-id="ac3be-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ac3be-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ac3be-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ac3be-122">Row index:</span></span>  <br/> |<span data-ttu-id="ac3be-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="ac3be-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="ac3be-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ac3be-124">Cell index:</span></span>  <br/> |<span data-ttu-id="ac3be-125">**visDocOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="ac3be-125">**visDocOutputFormat**</span></span> <br/> |
   

