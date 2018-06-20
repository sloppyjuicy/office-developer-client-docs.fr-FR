---
title: LockThemeFonts, cellule (Section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Empêche la cellule FontIndex dans la ligne de propriétés de thème de modification en appliquant un nouveau thème. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789045"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="27e14-104">LockThemeFonts, cellule (Section Protection)</span><span class="sxs-lookup"><span data-stu-id="27e14-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="27e14-105">Empêche la cellule **FontIndex** dans la ligne de **Propriétés de thème** de modification en appliquant un nouveau thème.</span><span class="sxs-lookup"><span data-stu-id="27e14-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="27e14-106">N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="27e14-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="27e14-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="27e14-107">**Value**</span></span>|<span data-ttu-id="27e14-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="27e14-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27e14-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="27e14-109">TRUE</span></span>  <br/> |<span data-ttu-id="27e14-110">La cellule **FontIndex** ne peut pas être modifiée de sa valeur actuelle, sauf si la modification directement dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="27e14-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="27e14-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="27e14-111">FALSE</span></span>  <br/> |<span data-ttu-id="27e14-112">La cellule **FontIndex** peut être modifiée à partir de sa valeur actuelle lorsque le thème est modifié.</span><span class="sxs-lookup"><span data-stu-id="27e14-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27e14-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="27e14-113">Remarks</span></span>

<span data-ttu-id="27e14-114">Pour obtenir une référence à la cellule **LockThemeFonts** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="27e14-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27e14-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="27e14-115">Cell name:</span></span>  <br/> | <span data-ttu-id="27e14-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="27e14-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="27e14-117">Pour obtenir une référence à la cellule **LockThemeFonts** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="27e14-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27e14-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="27e14-118">Section index:</span></span>  <br/> |<span data-ttu-id="27e14-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="27e14-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="27e14-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="27e14-120">Row index:</span></span>  <br/> |<span data-ttu-id="27e14-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="27e14-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="27e14-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="27e14-122">Cell index:</span></span>  <br/> |<span data-ttu-id="27e14-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="27e14-123">**visLockThemeFonts**</span></span> <br/> |
   

