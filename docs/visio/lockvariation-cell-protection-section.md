---
title: LockVariation, cellule (Section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Détermine si la variante de thème appliquée à la page ou la forme peut être modifiée en tant que valeur de type Boolean.
ms.openlocfilehash: c3c272a637f28aa4df43f6c23030d6676280138e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789041"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="c2982-103">LockVariation, cellule (Section Protection)</span><span class="sxs-lookup"><span data-stu-id="c2982-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="c2982-104">Détermine si la variante de thème appliquée à la page ou la forme peut être modifiée en tant que valeur de type Boolean.</span><span class="sxs-lookup"><span data-stu-id="c2982-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2982-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="c2982-105">TRUE</span></span>  <br/> |<span data-ttu-id="c2982-106">La variation actuelle appliquée à la page ou la forme ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="c2982-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="c2982-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="c2982-107">FALSE</span></span>  <br/> |<span data-ttu-id="c2982-108">La variation de la page ou la forme peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="c2982-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2982-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="c2982-109">Remarks</span></span>

<span data-ttu-id="c2982-110">Pour obtenir une référence à la cellule **LockVariation** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c2982-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2982-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c2982-111">Cell name:</span></span>  <br/> | <span data-ttu-id="c2982-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="c2982-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="c2982-113">Pour obtenir une référence à la cellule **LockVariation** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c2982-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c2982-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c2982-114">Section index:</span></span>  <br/> |<span data-ttu-id="c2982-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c2982-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c2982-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c2982-116">Row index:</span></span>  <br/> |<span data-ttu-id="c2982-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="c2982-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="c2982-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c2982-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c2982-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="c2982-119">**visLockVariation**</span></span> <br/> |
   

