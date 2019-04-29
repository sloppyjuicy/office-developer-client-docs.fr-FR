---
title: LockThemeFonts Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Empêche la cellule FontIndex de la ligne propriétés de thème d'être modifiée en appliquant un nouveau thème. N'empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421227"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="4c406-104">LockThemeFonts Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="4c406-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="4c406-105">Empêche la cellule **FontIndex** de la ligne **Propriétés de thème** d'être modifiée en appliquant un nouveau thème.</span><span class="sxs-lookup"><span data-stu-id="4c406-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="4c406-106">N'empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="4c406-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="4c406-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4c406-107">**Value**</span></span>|<span data-ttu-id="4c406-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="4c406-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4c406-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="4c406-109">TRUE</span></span>  <br/> |<span data-ttu-id="4c406-110">La cellule **FontIndex** ne peut pas être modifiée à partir de sa valeur actuelle sauf si elle a été modifiée directement dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="4c406-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="4c406-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="4c406-111">FALSE</span></span>  <br/> |<span data-ttu-id="4c406-112">La cellule **FontIndex** peut être modifiée à partir de sa valeur actuelle lorsque le thème est modifié.</span><span class="sxs-lookup"><span data-stu-id="4c406-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c406-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="4c406-113">Remarks</span></span>

<span data-ttu-id="4c406-114">Pour obtenir une référence à la cellule **LockThemeFonts** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="4c406-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c406-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="4c406-115">Cell name:</span></span>  <br/> | <span data-ttu-id="4c406-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="4c406-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="4c406-117">Pour obtenir une référence à la cellule **LockThemeFonts** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="4c406-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c406-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="4c406-118">Section index:</span></span>  <br/> |<span data-ttu-id="4c406-119">**Définis**</span><span class="sxs-lookup"><span data-stu-id="4c406-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4c406-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="4c406-120">Row index:</span></span>  <br/> |<span data-ttu-id="4c406-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="4c406-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="4c406-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4c406-122">Cell index:</span></span>  <br/> |<span data-ttu-id="4c406-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="4c406-123">**visLockThemeFonts**</span></span> <br/> |
   

