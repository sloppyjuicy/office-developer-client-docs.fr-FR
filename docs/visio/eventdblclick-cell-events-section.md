---
title: EventDblClick, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Cellule Event qui est évaluée lors d'un double-clic sur une forme.
ms.openlocfilehash: 623d1d095d3269cd9c82fa8d0d6601933a163f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788569"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="58c4c-103">EventDblClick, cellule (section Events)</span><span class="sxs-lookup"><span data-stu-id="58c4c-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="58c4c-104">Cellule Event qui est évaluée lors d'un double-clic sur une forme.</span><span class="sxs-lookup"><span data-stu-id="58c4c-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58c4c-105">Note</span><span class="sxs-lookup"><span data-stu-id="58c4c-105">Remarks</span></span>

<span data-ttu-id="58c4c-106">Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.</span><span class="sxs-lookup"><span data-stu-id="58c4c-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="58c4c-107">Pour obtenir une référence à la cellule EventDblClick par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="58c4c-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58c4c-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="58c4c-108">Cell name:</span></span>  <br/> | <span data-ttu-id="58c4c-109">EventDblClick</span><span class="sxs-lookup"><span data-stu-id="58c4c-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="58c4c-110">Pour obtenir une référence à la cellule EventDblClick par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="58c4c-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58c4c-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="58c4c-111">Section index:</span></span>  <br/> |<span data-ttu-id="58c4c-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="58c4c-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="58c4c-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="58c4c-113">Row index:</span></span>  <br/> |<span data-ttu-id="58c4c-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="58c4c-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="58c4c-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="58c4c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="58c4c-116">**visEvtCellDblClick**</span><span class="sxs-lookup"><span data-stu-id="58c4c-116">**visEvtCellDblClick**</span></span> <br/> |
   

