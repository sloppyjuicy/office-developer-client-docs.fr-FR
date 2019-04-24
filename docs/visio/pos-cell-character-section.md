---
title: Pos, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Détermine la position du texte de la forme par rapport à la ligne de base.
ms.openlocfilehash: d5f6823d6f55493095d29054745f62b579a47893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359814"
---
# <a name="pos-cell-character-section"></a><span data-ttu-id="ff647-103">Pos, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="ff647-103">Pos Cell (Character Section)</span></span>

<span data-ttu-id="ff647-104">Détermine la position du texte de la forme par rapport à la ligne de base.</span><span class="sxs-lookup"><span data-stu-id="ff647-104">Determines the position of the shape's text relative to the baseline.</span></span>
  
|<span data-ttu-id="ff647-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="ff647-105">**Value**</span></span>|<span data-ttu-id="ff647-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="ff647-106">**Description**</span></span>|<span data-ttu-id="ff647-107">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="ff647-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ff647-108">0</span><span class="sxs-lookup"><span data-stu-id="ff647-108">0</span></span>  <br/> | <span data-ttu-id="ff647-109">Normal</span><span class="sxs-lookup"><span data-stu-id="ff647-109">Normal position</span></span>  <br/> |<span data-ttu-id="ff647-110">**visPosNormal**</span><span class="sxs-lookup"><span data-stu-id="ff647-110">**visPosNormal**</span></span> <br/> |
| <span data-ttu-id="ff647-111">0,1</span><span class="sxs-lookup"><span data-stu-id="ff647-111">1</span></span>  <br/> | <span data-ttu-id="ff647-112">Exposant</span><span class="sxs-lookup"><span data-stu-id="ff647-112">Superscript</span></span>  <br/> |<span data-ttu-id="ff647-113">**visPosSuper**</span><span class="sxs-lookup"><span data-stu-id="ff647-113">**visPosSuper**</span></span> <br/> |
| <span data-ttu-id="ff647-114">n°2</span><span class="sxs-lookup"><span data-stu-id="ff647-114">2</span></span>  <br/> | <span data-ttu-id="ff647-115">Indice</span><span class="sxs-lookup"><span data-stu-id="ff647-115">Subscript</span></span>  <br/> |<span data-ttu-id="ff647-116">**visPosSub**</span><span class="sxs-lookup"><span data-stu-id="ff647-116">**visPosSub**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff647-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="ff647-117">Remarks</span></span>

<span data-ttu-id="ff647-118">Pour obtenir une référence à la cellule Pos par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ff647-118">To get a reference to the Pos cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff647-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ff647-119">Cell name:</span></span>  <br/> | <span data-ttu-id="ff647-120">Char. POS [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ff647-120">Char.Pos[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ff647-121">Pour obtenir une référence à la cellule Pos à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ff647-121">To get a reference to the Pos cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff647-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ff647-122">Section index:</span></span>  <br/> |<span data-ttu-id="ff647-123">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="ff647-123">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="ff647-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ff647-124">Row index:</span></span>  <br/> |<span data-ttu-id="ff647-125">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ff647-125">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ff647-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ff647-126">Cell index:</span></span>  <br/> |<span data-ttu-id="ff647-127">**visCharacterPos**</span><span class="sxs-lookup"><span data-stu-id="ff647-127">**visCharacterPos**</span></span> <br/> |
   

