---
title: LockVariation Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Détermine si la variante de thème appliquée à la page ou à la forme peut être modifiée, en tant que valeur booléenne.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427926"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="dd235-103">LockVariation Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="dd235-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="dd235-104">Détermine si la variante de thème appliquée à la page ou à la forme peut être modifiée, en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="dd235-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd235-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="dd235-105">TRUE</span></span>  <br/> |<span data-ttu-id="dd235-106">La variante actuelle appliquée à la page ou à la forme ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="dd235-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="dd235-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="dd235-107">FALSE</span></span>  <br/> |<span data-ttu-id="dd235-108">La variante de la page ou de la forme peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="dd235-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd235-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd235-109">Remarks</span></span>

<span data-ttu-id="dd235-110">Pour obtenir une référence à la cellule **LockVariation** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="dd235-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd235-111">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="dd235-111">Cell name:</span></span>  <br/> | <span data-ttu-id="dd235-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="dd235-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="dd235-113">Pour obtenir une référence à la cellule **LockVariation** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="dd235-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dd235-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="dd235-114">Section index:</span></span>  <br/> |<span data-ttu-id="dd235-115">**Définis**</span><span class="sxs-lookup"><span data-stu-id="dd235-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dd235-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="dd235-116">Row index:</span></span>  <br/> |<span data-ttu-id="dd235-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="dd235-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="dd235-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dd235-118">Cell index:</span></span>  <br/> |<span data-ttu-id="dd235-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="dd235-119">**visLockVariation**</span></span> <br/> |
   

