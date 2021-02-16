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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411504"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="c5e23-103">Initials, cellule (section Reviewer)</span><span class="sxs-lookup"><span data-stu-id="c5e23-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="c5e23-104">Contient les initiales du réviseur d’un document.</span><span class="sxs-lookup"><span data-stu-id="c5e23-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5e23-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5e23-105">Remarks</span></span>

<span data-ttu-id="c5e23-106">Cette valeur est par défaut les initiales  de la zone **Initiales** de l’onglet Général de la boîte de dialogue **Options Visio** (cliquez sur l’onglet Fichier, cliquez sur  **Options,** puis sur **Général).**</span><span class="sxs-lookup"><span data-stu-id="c5e23-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="c5e23-107">Pour obtenir une référence à la cellule Initials par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="c5e23-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5e23-108">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="c5e23-108">Cell name:</span></span>  <br/> | <span data-ttu-id="c5e23-109">Reviewer.Initials [  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c5e23-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c5e23-110">Pour obtenir une référence à la cellule Initials à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c5e23-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c5e23-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c5e23-111">Section index:</span></span>  <br/> |<span data-ttu-id="c5e23-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="c5e23-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="c5e23-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c5e23-113">Row index:</span></span>  <br/> |<span data-ttu-id="c5e23-114">**visRowReviewer**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c5e23-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c5e23-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c5e23-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c5e23-116">**visReviewerInitials**</span><span class="sxs-lookup"><span data-stu-id="c5e23-116">**visReviewerInitials**</span></span> <br/> |
   

