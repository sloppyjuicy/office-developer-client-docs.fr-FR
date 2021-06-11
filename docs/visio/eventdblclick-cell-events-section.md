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
ms.openlocfilehash: a50e88ecd8e432629e246f7038dfcc9626725cc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438217"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="d73e5-103">EventDblClick, cellule (section Events)</span><span class="sxs-lookup"><span data-stu-id="d73e5-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="d73e5-104">Cellule Event qui est évaluée lors d'un double-clic sur une forme.</span><span class="sxs-lookup"><span data-stu-id="d73e5-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d73e5-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d73e5-105">Remarks</span></span>

<span data-ttu-id="d73e5-106">Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.</span><span class="sxs-lookup"><span data-stu-id="d73e5-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="d73e5-107">Pour obtenir une référence à la cellule EventDblClick par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d73e5-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d73e5-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d73e5-108">Cell name:</span></span>  <br/> | <span data-ttu-id="d73e5-109">EventDblClick</span><span class="sxs-lookup"><span data-stu-id="d73e5-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="d73e5-110">Pour obtenir une référence à la cellule EventDblClick à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d73e5-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d73e5-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d73e5-111">Section index:</span></span>  <br/> |<span data-ttu-id="d73e5-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d73e5-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d73e5-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d73e5-113">Row index:</span></span>  <br/> |<span data-ttu-id="d73e5-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="d73e5-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="d73e5-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d73e5-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d73e5-116">**visEvtCellDblClick**</span><span class="sxs-lookup"><span data-stu-id="d73e5-116">**visEvtCellDblClick**</span></span> <br/> |
   

