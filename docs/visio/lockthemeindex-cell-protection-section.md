---
title: LockThemeIndex, cellule (Section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: ThemeIndex cellule dans la ligne de propriétés de thème empêche la modification en appliquant un nouveau thème ou en sélectionnant un nouveau jeu de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789027"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="8e423-104">LockThemeIndex, cellule (Section Protection)</span><span class="sxs-lookup"><span data-stu-id="8e423-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="8e423-105">**ThemeIndex** cellule dans la ligne de **Propriétés de thème** empêche la modification en appliquant un nouveau thème ou en sélectionnant un nouveau jeu de connecteur.</span><span class="sxs-lookup"><span data-stu-id="8e423-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="8e423-106">N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8e423-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="8e423-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8e423-107">**Value**</span></span>|<span data-ttu-id="8e423-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="8e423-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e423-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="8e423-109">TRUE</span></span>  <br/> |<span data-ttu-id="8e423-110">La cellule **ThemeIndex** ne peut pas être modifiée de sa valeur actuelle, sauf si la modification directement dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8e423-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="8e423-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="8e423-111">FALSE</span></span>  <br/> |<span data-ttu-id="8e423-112">La cellule **ThemeIndex** peut être modifiée à partir de sa valeur actuelle lorsque le thème est modifié.</span><span class="sxs-lookup"><span data-stu-id="8e423-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e423-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e423-113">Remarks</span></span>

<span data-ttu-id="8e423-114">Pour obtenir une référence à la cellule **LockThemeIndex** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="8e423-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e423-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8e423-115">Cell name:</span></span>  <br/> | <span data-ttu-id="8e423-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="8e423-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="8e423-117">Pour obtenir une référence à la cellule **LockThemeIndex** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8e423-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e423-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8e423-118">Section index:</span></span>  <br/> |<span data-ttu-id="8e423-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8e423-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8e423-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8e423-120">Row index:</span></span>  <br/> |<span data-ttu-id="8e423-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="8e423-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="8e423-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8e423-122">Cell index:</span></span>  <br/> |<span data-ttu-id="8e423-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="8e423-123">**visLockThemeIndex**</span></span> <br/> |
   

