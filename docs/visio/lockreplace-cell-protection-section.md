---
title: LockReplace Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indique si une forme peut participer à une opération de remplacement (en tant que forme cible ou de remplacement).
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404140"
---
# <a name="lockreplace-cell-protection-section"></a><span data-ttu-id="82e79-103">LockReplace Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="82e79-103">LockReplace Cell (Protection Section)</span></span>

<span data-ttu-id="82e79-104">Indique si une forme peut participer à une opération de remplacement (en tant que forme cible ou de remplacement).</span><span class="sxs-lookup"><span data-stu-id="82e79-104">Indicates whether a shape can participate in a replacement operation (as either a target or a replacement shape).</span></span> 
  
|<span data-ttu-id="82e79-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="82e79-105">**Value**</span></span>|<span data-ttu-id="82e79-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="82e79-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="82e79-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="82e79-107">TRUE</span></span>  <br/> |<span data-ttu-id="82e79-108">La forme ne peut pas être remplacée ou être utilisée comme une forme de remplacement.</span><span class="sxs-lookup"><span data-stu-id="82e79-108">The shape cannot be replaced or be used as a replacement shape.</span></span>  <br/> <span data-ttu-id="82e79-109">Pour une forme sur la zone de dessin, le bouton **modifier la forme** est désactivé lorsque la forme est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="82e79-109">For a shape on the canvas, the **Change Shape** button is disabled when the shape is selected.</span></span>  <br/> <span data-ttu-id="82e79-110">Pour une forme dans un gabarit, la forme n'apparaît pas en tant que forme de remplacement lorsque l'utilisateur clique sur le bouton **modifier la forme** .</span><span class="sxs-lookup"><span data-stu-id="82e79-110">For a shape on a stencil, the shape does not appear as a replacement shape when the **Change Shape** button is clicked.</span></span>  <br/> |
|<span data-ttu-id="82e79-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="82e79-111">FALSE</span></span>  <br/> |<span data-ttu-id="82e79-112">La forme peut être remplacée ou utilisée comme une forme de remplacement.</span><span class="sxs-lookup"><span data-stu-id="82e79-112">The shape can be replaced or used as a replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82e79-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="82e79-113">Remarks</span></span>

<span data-ttu-id="82e79-114">Pour obtenir une référence à la cellule **LockReplace** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="82e79-114">To get a reference to the **LockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="82e79-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="82e79-115">Cell name:</span></span>  <br/> | <span data-ttu-id="82e79-116">LockReplace</span><span class="sxs-lookup"><span data-stu-id="82e79-116">LockReplace</span></span>  <br/> |
   
<span data-ttu-id="82e79-117">Pour obtenir une référence à la cellule **LockReplace** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="82e79-117">To get a reference to the **LockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="82e79-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="82e79-118">Section index:</span></span>  <br/> |<span data-ttu-id="82e79-119">**Définis**</span><span class="sxs-lookup"><span data-stu-id="82e79-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="82e79-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="82e79-120">Row index:</span></span>  <br/> |<span data-ttu-id="82e79-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="82e79-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="82e79-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="82e79-122">Cell index:</span></span>  <br/> |<span data-ttu-id="82e79-123">**visLockReplace**</span><span class="sxs-lookup"><span data-stu-id="82e79-123">**visLockReplace**</span></span> <br/> |
   

