---
title: LockThemeConnectors, cellule (Section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Empêche la cellule ConnectorsSchemeIndex dans la ligne de propriétés de thème de modification en appliquant un nouveau thème ou en sélectionnant un nouveau jeu de connecteur. N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789024"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="5ed30-104">LockThemeConnectors, cellule (Section Protection)</span><span class="sxs-lookup"><span data-stu-id="5ed30-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="5ed30-105">Empêche la cellule **ConnectorsSchemeIndex** dans la ligne de **Propriétés de thème** de modification en appliquant un nouveau thème ou en sélectionnant un nouveau jeu de connecteur.</span><span class="sxs-lookup"><span data-stu-id="5ed30-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="5ed30-106">N’empêche pas les utilisateurs de modifier manuellement cette valeur dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="5ed30-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="5ed30-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5ed30-107">**Value**</span></span>|<span data-ttu-id="5ed30-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="5ed30-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ed30-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="5ed30-109">TRUE</span></span>  <br/> |<span data-ttu-id="5ed30-110">La cellule **ConnectorsSchemeIndex** ne peut pas être modifiée de sa valeur actuelle, sauf si la modification directement dans la feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="5ed30-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="5ed30-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="5ed30-111">FALSE</span></span>  <br/> |<span data-ttu-id="5ed30-112">La cellule **ConnectorsSchemeIndex** peut être modifiée à partir de sa valeur actuelle par le biais de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5ed30-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ed30-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="5ed30-113">Remarks</span></span>

<span data-ttu-id="5ed30-114">Pour obtenir une référence à la cellule **LockThemeConnectors** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="5ed30-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ed30-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5ed30-115">Cell name:</span></span>  <br/> | <span data-ttu-id="5ed30-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="5ed30-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="5ed30-117">Pour obtenir une référence à la cellule **LockThemeConnectors** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5ed30-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ed30-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5ed30-118">Section index:</span></span>  <br/> |<span data-ttu-id="5ed30-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5ed30-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5ed30-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5ed30-120">Row index:</span></span>  <br/> |<span data-ttu-id="5ed30-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="5ed30-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="5ed30-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5ed30-122">Cell index:</span></span>  <br/> |<span data-ttu-id="5ed30-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="5ed30-123">**visLockThemeConnectors**</span></span> <br/> |
   

