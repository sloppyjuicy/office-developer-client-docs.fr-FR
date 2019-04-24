---
title: DontMoveChildren, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Détermine la possibilité ou non de faire glisser, à l'aide de la souris, des formes dans un groupe.
ms.openlocfilehash: 2b15d75a98b5f5a72bce8b80758d27b197a346ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338583"
---
# <a name="dontmovechildren-cell-group-properties-section"></a><span data-ttu-id="7b70f-103">DontMoveChildren, cellule (section Group Properties)</span><span class="sxs-lookup"><span data-stu-id="7b70f-103">DontMoveChildren Cell (Group Properties Section)</span></span>

<span data-ttu-id="7b70f-104">Détermine la possibilité ou non de faire glisser, à l'aide de la souris, des formes dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="7b70f-104">Determines whether you can drag shapes in a group using the mouse.</span></span>
  
|<span data-ttu-id="7b70f-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="7b70f-105">**Value**</span></span>|<span data-ttu-id="7b70f-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="7b70f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7b70f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7b70f-107">TRUE</span></span>  <br/> | <span data-ttu-id="7b70f-108">Les formes d'un groupe ne peuvent pas être déplacées avec la souris.</span><span class="sxs-lookup"><span data-stu-id="7b70f-108">Don't allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
| <span data-ttu-id="7b70f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7b70f-109">FALSE</span></span>  <br/> | <span data-ttu-id="7b70f-110">Les formes d'un groupe peuvent être déplacées avec la souris.</span><span class="sxs-lookup"><span data-stu-id="7b70f-110">Allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b70f-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="7b70f-111">Remarks</span></span>

<span data-ttu-id="7b70f-112">Lorsque cette cellule est réglée sur TRUE, vous pouvez retourner, faire pivoter, redimensionner ou repositionner les formes d'un groupe à l'aide des autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="7b70f-112">When the value of this cell is TRUE, you can still flip, rotate, resize, or reposition shapes in groups using other methods.</span></span>
  
<span data-ttu-id="7b70f-113">Cette cellule a pour valeur TRUE pour les groupes de formes de base et ceux d'instances de formes de base créées avec les versions de Visio antérieures à Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="7b70f-113">The value of this cell is TRUE for groups in masters and groups in instances of masters that were created in versions of Visio earlier than version 2000.</span></span>
  
<span data-ttu-id="7b70f-114">Pour obtenir une référence à la cellule DontMoveChildren par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7b70f-114">To get a reference to the DontMoveChildren cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b70f-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7b70f-115">Cell name:</span></span>  <br/> | <span data-ttu-id="7b70f-116">DontMoveChildren</span><span class="sxs-lookup"><span data-stu-id="7b70f-116">DontMoveChildren</span></span>  <br/> |
   
<span data-ttu-id="7b70f-117">Pour obtenir une référence à la cellule DontMoveChildren à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7b70f-117">To get a reference to the DontMoveChildren cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b70f-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7b70f-118">Section index:</span></span>  <br/> |<span data-ttu-id="7b70f-119">**Définis**</span><span class="sxs-lookup"><span data-stu-id="7b70f-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7b70f-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7b70f-120">Row index:</span></span>  <br/> |<span data-ttu-id="7b70f-121">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="7b70f-121">**visRowGroup**</span></span> <br/> |
| <span data-ttu-id="7b70f-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7b70f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="7b70f-123">**visGroupDontMoveChildren**</span><span class="sxs-lookup"><span data-stu-id="7b70f-123">**visGroupDontMoveChildren**</span></span> <br/> |
   

