---
title: LockRotate, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Empêche les formes 2D en rotation avec la poignée de rotation ou la faire pivoter à gauche de 90° ou commande de 90° faire pivoter à droite.
ms.openlocfilehash: 450fe4786594472d018b705df4678fe636390ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789015"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="0a874-103">LockRotate, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="0a874-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="0a874-104">Verrouille avec la poignée de rotation ou la **faire pivoter à gauche de 90 °** ou **faire pivoter à droite de 90 °** commande pivoter les formes 2D.</span><span class="sxs-lookup"><span data-stu-id="0a874-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="0a874-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="0a874-105">**Value**</span></span>|<span data-ttu-id="0a874-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="0a874-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0a874-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0a874-107">TRUE</span></span>  <br/> | <span data-ttu-id="0a874-108">La rotation de la forme est impossible.</span><span class="sxs-lookup"><span data-stu-id="0a874-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="0a874-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0a874-109">FALSE</span></span>  <br/> | <span data-ttu-id="0a874-110">La rotation de la forme est possible (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="0a874-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a874-111">Note</span><span class="sxs-lookup"><span data-stu-id="0a874-111">Remarks</span></span>

<span data-ttu-id="0a874-p101">La cellule LockRotate n'empêche pas de faire pivoter une forme 1D lorsque vous faites glisser une extrémité. Pour verrouiller une forme 1D afin d'empêcher sa rotation, attribuez une valeur différente de zéro à la cellule LockWidth (TRUE).</span><span class="sxs-lookup"><span data-stu-id="0a874-p101">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged. To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="0a874-114">Pour obtenir une référence à la cellule LockRotate par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="0a874-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a874-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="0a874-115">Cell name:</span></span>  <br/> | <span data-ttu-id="0a874-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="0a874-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="0a874-117">Pour obtenir une référence à la cellule LockRotate par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="0a874-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a874-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="0a874-118">Section index:</span></span>  <br/> |<span data-ttu-id="0a874-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0a874-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0a874-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="0a874-120">Row index:</span></span>  <br/> |<span data-ttu-id="0a874-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="0a874-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="0a874-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0a874-122">Cell index:</span></span>  <br/> |<span data-ttu-id="0a874-123">**visLockRotate**</span><span class="sxs-lookup"><span data-stu-id="0a874-123">**visLockRotate**</span></span> <br/> |
   

