---
title: Initials, cellule (section Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Contient les initiales du réviseur d’un document.
ms.openlocfilehash: 65f0082219c8d6adca55af86c027b2ec5642fb5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788842"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="5ce70-103">Initials, cellule (section Reviewer)</span><span class="sxs-lookup"><span data-stu-id="5ce70-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="5ce70-104">Contient les initiales du réviseur d’un document.</span><span class="sxs-lookup"><span data-stu-id="5ce70-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ce70-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="5ce70-105">Remarks</span></span>

<span data-ttu-id="5ce70-106">La valeur par défaut aux initiales qui apparaissent dans la zone **initiales** sous l’onglet **Général** dans la boîte de dialogue **Options Visio** (cliquez sur l’onglet **fichier** , cliquez sur **Options**, puis cliquez sur **Général** ).</span><span class="sxs-lookup"><span data-stu-id="5ce70-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="5ce70-107">Pour obtenir une référence à la cellule Initials par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="5ce70-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ce70-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5ce70-108">Cell name:</span></span>  <br/> | <span data-ttu-id="5ce70-109">Reviewer.Initials [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5ce70-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5ce70-110">Pour obtenir une référence à la cellule Initials par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5ce70-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ce70-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5ce70-111">Section index:</span></span>  <br/> |<span data-ttu-id="5ce70-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="5ce70-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="5ce70-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5ce70-113">Row index:</span></span>  <br/> |<span data-ttu-id="5ce70-114">**visRowReviewer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5ce70-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5ce70-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5ce70-115">Cell index:</span></span>  <br/> |<span data-ttu-id="5ce70-116">**visReviewerInitials**</span><span class="sxs-lookup"><span data-stu-id="5ce70-116">**visReviewerInitials**</span></span> <br/> |
   

