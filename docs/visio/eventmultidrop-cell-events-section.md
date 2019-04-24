---
title: EventMultiDrop, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337190"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="d9468-102">EventMultiDrop, cellule (section Events)</span><span class="sxs-lookup"><span data-stu-id="d9468-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="d9468-103">Cellule Event qui est évaluée lorsque plusieurs formes sont déposées sur la page de dessin, soit comme instances, soit lorsque des formes sont dupliquées ou collées.</span><span class="sxs-lookup"><span data-stu-id="d9468-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="d9468-104">Les cellules événements ne sont évaluées que lorsque l'événement se produit et non lorsque la formule est saisie.</span><span class="sxs-lookup"><span data-stu-id="d9468-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="d9468-105">Pour faire référence à la cellule EventMultiDrop par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d9468-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9468-106">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d9468-106">Cell name:</span></span>  <br/> |<span data-ttu-id="d9468-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="d9468-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="d9468-108">Pour faire référence à la cellule EventMultiDrop par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d9468-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9468-109">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d9468-109">Section index:</span></span>  <br/> |<span data-ttu-id="d9468-110">**Définis**</span><span class="sxs-lookup"><span data-stu-id="d9468-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d9468-111">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d9468-111">Row index:</span></span>  <br/> |<span data-ttu-id="d9468-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="d9468-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="d9468-113">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d9468-113">Cell index:</span></span>  <br/> |<span data-ttu-id="d9468-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="d9468-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

