---
title: LockThemeColors, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70001
localization_priority: Normal
ms.assetid: 22cedeb3-58b5-3932-9252-5c9dd3e163e3
ms.openlocfilehash: 81091ea33be2158435d240ba14f3c97e8f3fcc39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348285"
---
# <a name="lockthemecolors-cell-protection-section"></a><span data-ttu-id="bd3c5-102">LockThemeColors, cellule (section Protection)</span><span class="sxs-lookup"><span data-stu-id="bd3c5-102">LockThemeColors Cell (Protection Section)</span></span>

<span data-ttu-id="bd3c5-103">Empêche l'application de couleurs de thème à la forme.</span><span class="sxs-lookup"><span data-stu-id="bd3c5-103">Prevents application of theme colors to the shape.</span></span> 
  
<span data-ttu-id="bd3c5-104">La valeur de la cellule LockThemeColors correspond au paramétrage de la case à cocher **Contre les couleurs du thème** de la boîte de dialogue **Protection**.</span><span class="sxs-lookup"><span data-stu-id="bd3c5-104">The value of the LockThemeColors cell corresponds to the **From theme colors** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="bd3c5-105">Pour faire référence à la cellule LockThemeColors par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :

</span><span class="sxs-lookup"><span data-stu-id="bd3c5-105">To refer to the LockThemeColors cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd3c5-106">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bd3c5-106">Cell name:</span></span>  <br/> |<span data-ttu-id="bd3c5-107">LockThemeColors</span><span class="sxs-lookup"><span data-stu-id="bd3c5-107">LockThemeColors</span></span>  <br/> |
   
<span data-ttu-id="bd3c5-108">Pour faire référence à la cellule LockThemeColors par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bd3c5-108">To refer to the LockThemeColors cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd3c5-109">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bd3c5-109">Section index:</span></span>  <br/> |<span data-ttu-id="bd3c5-110">**Définis**</span><span class="sxs-lookup"><span data-stu-id="bd3c5-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bd3c5-111">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bd3c5-111">Row index:</span></span>  <br/> |<span data-ttu-id="bd3c5-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="bd3c5-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="bd3c5-113">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bd3c5-113">Cell index:</span></span>  <br/> |<span data-ttu-id="bd3c5-114">**visLockThemeColors**</span><span class="sxs-lookup"><span data-stu-id="bd3c5-114">**visLockThemeColors**</span></span> <br/> |
   

