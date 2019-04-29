---
title: EventDrop, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Cellule Event qui est évaluée lorsqu'une forme est insérée sur la page de dessin, soit comme instance, soit lorsqu'elle est dupliquée ou collée.
ms.openlocfilehash: f1433394dbd58c7c4422c6bca1e79a4f2c8e0c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408592"
---
# <a name="eventdrop-cell-events-section"></a><span data-ttu-id="8a005-103">EventDrop, cellule (section Events)</span><span class="sxs-lookup"><span data-stu-id="8a005-103">EventDrop Cell (Events Section)</span></span>

<span data-ttu-id="8a005-104">Cellule Event qui est évaluée lorsqu'une forme est insérée sur la page de dessin, soit comme instance, soit lorsqu'elle est dupliquée ou collée.</span><span class="sxs-lookup"><span data-stu-id="8a005-104">An event cell that is evaluated when a shape is dropped on the drawing page, either as an instance or when the shape is duplicated or pasted.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a005-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="8a005-105">Remarks</span></span>

<span data-ttu-id="8a005-106">Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.</span><span class="sxs-lookup"><span data-stu-id="8a005-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="8a005-107">Pour obtenir une référence à la cellule EventDrop par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="8a005-107">To get a reference to the EventDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8a005-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8a005-108">Cell name:</span></span>  <br/> | <span data-ttu-id="8a005-109">EventDrop</span><span class="sxs-lookup"><span data-stu-id="8a005-109">EventDrop</span></span>  <br/> |
   
<span data-ttu-id="8a005-110">Pour obtenir une référence à la cellule EventDrop à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8a005-110">To get a reference to the EventDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8a005-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8a005-111">Section index:</span></span>  <br/> |<span data-ttu-id="8a005-112">**Définis**</span><span class="sxs-lookup"><span data-stu-id="8a005-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8a005-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8a005-113">Row index:</span></span>  <br/> |<span data-ttu-id="8a005-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="8a005-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="8a005-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8a005-115">Cell index:</span></span>  <br/> |<span data-ttu-id="8a005-116">**visEvtCellDrop**</span><span class="sxs-lookup"><span data-stu-id="8a005-116">**visEvtCellDrop**</span></span> <br/> |
   

