---
title: EventMultiDrop, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416719"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="f90f2-102">EventMultiDrop, cellule (section Events)</span><span class="sxs-lookup"><span data-stu-id="f90f2-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="f90f2-103">Cellule d’événement évaluée lorsque plusieurs formes sont abandonnées sur la page de dessin, soit en tant qu’instances, soit lorsque des formes sont dupliquées ou copiées.</span><span class="sxs-lookup"><span data-stu-id="f90f2-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="f90f2-104">Les cellules événements ne sont évaluées que lorsque l'événement se produit et non lorsque la formule est saisie.</span><span class="sxs-lookup"><span data-stu-id="f90f2-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="f90f2-105">Pour faire référence à la cellule EventMultiDrop par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f90f2-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f90f2-106">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f90f2-106">Cell name:</span></span>  <br/> |<span data-ttu-id="f90f2-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="f90f2-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="f90f2-108">Pour faire référence à la cellule EventMultiDrop par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f90f2-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f90f2-109">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f90f2-109">Section index:</span></span>  <br/> |<span data-ttu-id="f90f2-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f90f2-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f90f2-111">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f90f2-111">Row index:</span></span>  <br/> |<span data-ttu-id="f90f2-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="f90f2-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="f90f2-113">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f90f2-113">Cell index:</span></span>  <br/> |<span data-ttu-id="f90f2-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="f90f2-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

