---
title: Color, cellule (section Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Une valeur RVB qui représente la couleur attribuée à la balise du réviseur d’un document.
ms.openlocfilehash: a8771bb35cfc1b57990f24e1a0a3d677f9cffc0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788276"
---
# <a name="color-cell-reviewer-section"></a><span data-ttu-id="bd93e-103">Color, cellule (section Reviewer)</span><span class="sxs-lookup"><span data-stu-id="bd93e-103">Color Cell (Reviewer Section)</span></span>

<span data-ttu-id="bd93e-104">Une valeur RVB qui représente la couleur attribuée à la balise du réviseur d’un document.</span><span class="sxs-lookup"><span data-stu-id="bd93e-104">An RGB value that represents the color assigned to a document reviewer's markup.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bd93e-105">Note</span><span class="sxs-lookup"><span data-stu-id="bd93e-105">Remarks</span></span>

<span data-ttu-id="bd93e-p101">Les couleurs sont attribuées aux réviseurs selon la séquence suivante : rouge, bleu, vert, violet, orange, turquoise, gris. Ces couleurs se succèdent à nouveau pour chaque autre réviseur.</span><span class="sxs-lookup"><span data-stu-id="bd93e-p101">Colors are assigned to reviewers in the following sequence: red, blue, green, violet, orange, turquoise, gray. These colors are cycled through again for any remaining reviewers.</span></span> 
  
<span data-ttu-id="bd93e-108">Les commentaires entrés sur la page de dessin d'origine sont toujours de couleur jaune, peu importe la couleur attribuée à un réviseur dans la cellule Color.</span><span class="sxs-lookup"><span data-stu-id="bd93e-108">Comments entered on the original drawing page are always colored yellow, regardless of the color assigned to a reviewer in the Color cell.</span></span> 
  
<span data-ttu-id="bd93e-109">Pour obtenir une référence à la cellule Color par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="bd93e-109">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd93e-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bd93e-110">Cell name:</span></span>  <br/> | <span data-ttu-id="bd93e-111">Reviewer.Color [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bd93e-111">Reviewer.Color [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bd93e-112">Pour obtenir une référence à la cellule Color par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bd93e-112">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd93e-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bd93e-113">Section index:</span></span>  <br/> |<span data-ttu-id="bd93e-114">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="bd93e-114">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="bd93e-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bd93e-115">Row index:</span></span>  <br/> |<span data-ttu-id="bd93e-116">**visRowReviewer** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bd93e-116">**visRowReviewer** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bd93e-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bd93e-117">Cell index:</span></span>  <br/> |<span data-ttu-id="bd93e-118">**visReviewerColor**</span><span class="sxs-lookup"><span data-stu-id="bd93e-118">**visReviewerColor**</span></span> <br/> |
   

