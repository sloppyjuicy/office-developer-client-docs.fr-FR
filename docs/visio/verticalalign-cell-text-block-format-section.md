---
title: VerticalAlign, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Détermine l'alignement vertical du texte dans le bloc de texte.
ms.openlocfilehash: 954a0cf0b80d6b675dcc016997f1923041069eac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356140"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="607c0-103">VerticalAlign, cellule (section Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="607c0-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="607c0-104">Détermine l'alignement vertical du texte dans le bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="607c0-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="607c0-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="607c0-105">**Value**</span></span>|<span data-ttu-id="607c0-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="607c0-106">**Description**</span></span>|<span data-ttu-id="607c0-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="607c0-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="607c0-108">0</span><span class="sxs-lookup"><span data-stu-id="607c0-108">0</span></span>  <br/> | <span data-ttu-id="607c0-109">Haut</span><span class="sxs-lookup"><span data-stu-id="607c0-109">Top</span></span>  <br/> |<span data-ttu-id="607c0-110">**visVertTop**</span><span class="sxs-lookup"><span data-stu-id="607c0-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="607c0-111">0,1</span><span class="sxs-lookup"><span data-stu-id="607c0-111">1</span></span>  <br/> | <span data-ttu-id="607c0-112">Centre</span><span class="sxs-lookup"><span data-stu-id="607c0-112">Middle</span></span>  <br/> |<span data-ttu-id="607c0-113">**visVertMiddle**</span><span class="sxs-lookup"><span data-stu-id="607c0-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="607c0-114">n°2</span><span class="sxs-lookup"><span data-stu-id="607c0-114">2</span></span>  <br/> | <span data-ttu-id="607c0-115">Inférieures</span><span class="sxs-lookup"><span data-stu-id="607c0-115">Bottom</span></span>  <br/> |<span data-ttu-id="607c0-116">**visVertBottom**</span><span class="sxs-lookup"><span data-stu-id="607c0-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="607c0-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="607c0-117">Remarks</span></span>

<span data-ttu-id="607c0-118">Pour obtenir une référence à la cellule VerticalAlign par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="607c0-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="607c0-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="607c0-119">Cell name:</span></span>  <br/> | <span data-ttu-id="607c0-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="607c0-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="607c0-121">Pour obtenir une référence à la cellule VerticalAlign par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="607c0-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="607c0-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="607c0-122">Section index:</span></span>  <br/> |<span data-ttu-id="607c0-123">**Définis**</span><span class="sxs-lookup"><span data-stu-id="607c0-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="607c0-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="607c0-124">Row index:</span></span>  <br/> |<span data-ttu-id="607c0-125">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="607c0-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="607c0-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="607c0-126">Cell index:</span></span>  <br/> |<span data-ttu-id="607c0-127">**visTxtBlkVerticalAlign**</span><span class="sxs-lookup"><span data-stu-id="607c0-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

