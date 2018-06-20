---
title: EventMultiDrop, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: e44cd18c3f7673761f457db9cd4bfe00a8ab89bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788584"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="dec8a-102">EventMultiDrop, cellule (section Events)</span><span class="sxs-lookup"><span data-stu-id="dec8a-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="dec8a-103">Cellule event qui est évaluée lorsque plusieurs formes sont insérées sur la page de dessin en tant qu’instances ou lorsqu’elles sont dupliquées ou collées.</span><span class="sxs-lookup"><span data-stu-id="dec8a-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="dec8a-104">Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.</span><span class="sxs-lookup"><span data-stu-id="dec8a-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="dec8a-105">Pour faire référence à la cellule EventMultiDrop par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="dec8a-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dec8a-106">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dec8a-106">Cell name:</span></span>  <br/> |<span data-ttu-id="dec8a-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="dec8a-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="dec8a-108">Pour faire référence à la cellule EventMultiDrop par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dec8a-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dec8a-109">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="dec8a-109">Section index:</span></span>  <br/> |<span data-ttu-id="dec8a-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dec8a-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dec8a-111">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="dec8a-111">Row index:</span></span>  <br/> |<span data-ttu-id="dec8a-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="dec8a-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="dec8a-113">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dec8a-113">Cell index:</span></span>  <br/> |<span data-ttu-id="dec8a-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="dec8a-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

