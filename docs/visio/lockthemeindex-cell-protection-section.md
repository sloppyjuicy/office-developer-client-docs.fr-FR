---
title: LockThemeIndex Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Empêche la cellule ThemeIndex de la ligne propriétés du thème d'être modifiée en appliquant un nouveau thème ou en sélectionnant un nouveau modèle de connecteur. N'empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411238"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="8316e-104">LockThemeIndex Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="8316e-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="8316e-105">Empêche la cellule **ThemeIndex** de la ligne **Propriétés du thème** d'être modifiée en appliquant un nouveau thème ou en sélectionnant un nouveau modèle de connecteur.</span><span class="sxs-lookup"><span data-stu-id="8316e-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="8316e-106">N'empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8316e-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="8316e-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8316e-107">**Value**</span></span>|<span data-ttu-id="8316e-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="8316e-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8316e-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="8316e-109">TRUE</span></span>  <br/> |<span data-ttu-id="8316e-110">La cellule **ThemeIndex** ne peut pas être modifiée à partir de sa valeur actuelle sauf si elle a été modifiée directement dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8316e-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="8316e-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="8316e-111">FALSE</span></span>  <br/> |<span data-ttu-id="8316e-112">La cellule **ThemeIndex** peut être modifiée à partir de sa valeur actuelle lorsque le thème est modifié.</span><span class="sxs-lookup"><span data-stu-id="8316e-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8316e-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="8316e-113">Remarks</span></span>

<span data-ttu-id="8316e-114">Pour obtenir une référence à la cellule **LockThemeIndex** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="8316e-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8316e-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="8316e-115">Cell name:</span></span>  <br/> | <span data-ttu-id="8316e-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="8316e-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="8316e-117">Pour obtenir une référence à la cellule **LockThemeIndex** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="8316e-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8316e-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8316e-118">Section index:</span></span>  <br/> |<span data-ttu-id="8316e-119">**Définis**</span><span class="sxs-lookup"><span data-stu-id="8316e-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8316e-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8316e-120">Row index:</span></span>  <br/> |<span data-ttu-id="8316e-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="8316e-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="8316e-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8316e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="8316e-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="8316e-123">**visLockThemeIndex**</span></span> <br/> |
   

