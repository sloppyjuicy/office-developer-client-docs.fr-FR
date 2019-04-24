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
ms.openlocfilehash: ddca3697dfcf1f422efacbe395c18f1a6b8ac48c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335293"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="97c8b-103">Initials, cellule (section Reviewer)</span><span class="sxs-lookup"><span data-stu-id="97c8b-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="97c8b-104">Contient les initiales du réviseur d’un document.</span><span class="sxs-lookup"><span data-stu-id="97c8b-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="97c8b-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="97c8b-105">Remarks</span></span>

<span data-ttu-id="97c8b-106">Cette valeur est définie par défaut sur les initiales figurant dans la zone **initiales** de l'onglet **général** de la boîte de dialogue **options Visio** (cliquez sur l'onglet **fichier** , sur **options**, puis sur **général** ).</span><span class="sxs-lookup"><span data-stu-id="97c8b-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="97c8b-107">Pour obtenir une référence à la cellule Initials par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="97c8b-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97c8b-108">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="97c8b-108">Cell name:</span></span>  <br/> | <span data-ttu-id="97c8b-109">Reviewer. Initials [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="97c8b-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="97c8b-110">Pour obtenir une référence à la cellule Initials à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="97c8b-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97c8b-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="97c8b-111">Section index:</span></span>  <br/> |<span data-ttu-id="97c8b-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="97c8b-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="97c8b-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="97c8b-113">Row index:</span></span>  <br/> |<span data-ttu-id="97c8b-114">**visRowReviewer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="97c8b-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="97c8b-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="97c8b-115">Cell index:</span></span>  <br/> |<span data-ttu-id="97c8b-116">**visReviewerInitials**</span><span class="sxs-lookup"><span data-stu-id="97c8b-116">**visReviewerInitials**</span></span> <br/> |
   

