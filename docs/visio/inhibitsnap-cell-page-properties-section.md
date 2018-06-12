---
title: InhibitSnap, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Détermine si les formes d'une page en premier plan s'alignent sur d'autres objets de la page et sur des formes de la page d'arrière-plan.
ms.openlocfilehash: b95dafda9ebef36db34f60585ab3ed2164ade415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788831"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="c6bfa-103">InhibitSnap, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="c6bfa-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="c6bfa-104">Détermine si les formes d'une page en premier plan s'alignent sur d'autres objets de la page et sur des formes de la page d'arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c6bfa-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="c6bfa-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c6bfa-105">**Value**</span></span>|<span data-ttu-id="c6bfa-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="c6bfa-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c6bfa-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c6bfa-107">TRUE</span></span>  <br/> | <span data-ttu-id="c6bfa-108">Interdit tout alignement sur la page à l'exception de l'alignement sur la règle et sur la grille.</span><span class="sxs-lookup"><span data-stu-id="c6bfa-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="c6bfa-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6bfa-109">FALSE</span></span>  <br/> | <span data-ttu-id="c6bfa-110">Active l'alignement.</span><span class="sxs-lookup"><span data-stu-id="c6bfa-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6bfa-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c6bfa-111">Remarks</span></span>

<span data-ttu-id="c6bfa-112">Pour obtenir une référence à la cellule InhibitSnap par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c6bfa-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6bfa-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c6bfa-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c6bfa-114">InhibitSnap</span><span class="sxs-lookup"><span data-stu-id="c6bfa-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="c6bfa-115">Pour obtenir une référence à la cellule InhibitSnap par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c6bfa-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6bfa-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c6bfa-116">Section index:</span></span>  <br/> |<span data-ttu-id="c6bfa-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c6bfa-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c6bfa-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c6bfa-118">Row index:</span></span>  <br/> |<span data-ttu-id="c6bfa-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="c6bfa-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="c6bfa-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c6bfa-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c6bfa-121">**visPageInhibitSnap**</span><span class="sxs-lookup"><span data-stu-id="c6bfa-121">**visPageInhibitSnap**</span></span> <br/> |
   

