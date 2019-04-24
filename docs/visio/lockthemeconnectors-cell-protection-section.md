---
title: LockThemeConnectors Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Empêche la cellule ConnectorsSchemeIndex de la ligne propriétés de thème d'être modifiée en appliquant un nouveau thème ou en sélectionnant un nouveau modèle de connecteur. N'empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348236"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="ed691-104">LockThemeConnectors Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="ed691-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="ed691-105">Empêche la cellule **ConnectorsSchemeIndex** de la ligne **Propriétés de thème** d'être modifiée en appliquant un nouveau thème ou en sélectionnant un nouveau modèle de connecteur.</span><span class="sxs-lookup"><span data-stu-id="ed691-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="ed691-106">N'empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ed691-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="ed691-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="ed691-107">**Value**</span></span>|<span data-ttu-id="ed691-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="ed691-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ed691-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="ed691-109">TRUE</span></span>  <br/> |<span data-ttu-id="ed691-110">La cellule **ConnectorsSchemeIndex** ne peut pas être modifiée à partir de sa valeur actuelle sauf si elle a été modifiée directement dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ed691-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="ed691-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="ed691-111">FALSE</span></span>  <br/> |<span data-ttu-id="ed691-112">La cellule **ConnectorsSchemeIndex** peut être modifiée à partir de sa valeur actuelle via l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed691-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed691-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="ed691-113">Remarks</span></span>

<span data-ttu-id="ed691-114">Pour obtenir une référence à la cellule **LockThemeConnectors** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="ed691-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed691-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="ed691-115">Cell name:</span></span>  <br/> | <span data-ttu-id="ed691-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="ed691-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="ed691-117">Pour obtenir une référence à la cellule **LockThemeConnectors** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="ed691-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed691-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ed691-118">Section index:</span></span>  <br/> |<span data-ttu-id="ed691-119">**Définis**</span><span class="sxs-lookup"><span data-stu-id="ed691-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ed691-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ed691-120">Row index:</span></span>  <br/> |<span data-ttu-id="ed691-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="ed691-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="ed691-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ed691-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ed691-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="ed691-123">**visLockThemeConnectors**</span></span> <br/> |
   

