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
description: Empêche de faire pivoter les formes 2D avec la poignée de rotation ou la commande Faire pivoter à gauche de 90° ou Faire pivoter à droite de 90°.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404672"
---
# <a name="lockrotate-cell-protection-section"></a><span data-ttu-id="93857-103">LockRotate, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="93857-103">LockRotate Cell (Protection Section)</span></span>

<span data-ttu-id="93857-104">Empêche de faire pivoter les formes 2D avec la poignée de rotation ou la commande **Faire pivoter à gauche de 90°** ou **Faire pivoter à droite de 90°**.</span><span class="sxs-lookup"><span data-stu-id="93857-104">Locks 2-D shapes against being rotated with the rotation handle or the **Rotate Left 90°** or **Rotate Right 90°** command.</span></span> 
  
|<span data-ttu-id="93857-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="93857-105">**Value**</span></span>|<span data-ttu-id="93857-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="93857-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="93857-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="93857-107">TRUE</span></span>  <br/> | <span data-ttu-id="93857-108">La rotation de la forme est impossible.</span><span class="sxs-lookup"><span data-stu-id="93857-108">Shape cannot be rotated.</span></span>  <br/> |
| <span data-ttu-id="93857-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="93857-109">FALSE</span></span>  <br/> | <span data-ttu-id="93857-110">La rotation de la forme est possible (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="93857-110">Shape can be rotated (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93857-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="93857-111">Remarks</span></span>

<span data-ttu-id="93857-p101">La cellule LockRotate n'empêche pas de faire pivoter une forme 1D lorsque vous faites glisser une extrémité. Pour verrouiller une forme 1D afin d'empêcher sa rotation, attribuez une valeur différente de zéro à la cellule LockWidth (TRUE).</span><span class="sxs-lookup"><span data-stu-id="93857-p101">The LockRotate cell does not prevent a 1-D shape from being rotated when an endpoint is dragged. To lock a 1-D shape against rotation, set the LockWidth cell to a non-zero value (TRUE).</span></span>
  
<span data-ttu-id="93857-114">Pour obtenir une référence à la cellule LockRotate par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="93857-114">To get a reference to the LockRotate cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93857-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="93857-115">Cell name:</span></span>  <br/> | <span data-ttu-id="93857-116">LockRotate</span><span class="sxs-lookup"><span data-stu-id="93857-116">LockRotate</span></span>  <br/> |
   
<span data-ttu-id="93857-117">Pour obtenir une référence à la cellule LockRotate à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="93857-117">To get a reference to the LockRotate cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="93857-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="93857-118">Section index:</span></span>  <br/> |<span data-ttu-id="93857-119">**Définis**</span><span class="sxs-lookup"><span data-stu-id="93857-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="93857-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="93857-120">Row index:</span></span>  <br/> |<span data-ttu-id="93857-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="93857-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="93857-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="93857-122">Cell index:</span></span>  <br/> |<span data-ttu-id="93857-123">**visLockRotate**</span><span class="sxs-lookup"><span data-stu-id="93857-123">**visLockRotate**</span></span> <br/> |
   

