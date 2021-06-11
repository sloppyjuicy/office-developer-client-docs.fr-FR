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
description: Valeur RVB qui représente la couleur affectée au code d’un réviseur de documents.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430538"
---
# <a name="color-cell-reviewer-section"></a><span data-ttu-id="60ff0-103">Color, cellule (section Reviewer)</span><span class="sxs-lookup"><span data-stu-id="60ff0-103">Color Cell (Reviewer Section)</span></span>

<span data-ttu-id="60ff0-104">Valeur RVB qui représente la couleur affectée au code d’un réviseur de documents.</span><span class="sxs-lookup"><span data-stu-id="60ff0-104">An RGB value that represents the color assigned to a document reviewer's markup.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="60ff0-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="60ff0-105">Remarks</span></span>

<span data-ttu-id="60ff0-p101">Les couleurs sont attribuées aux réviseurs selon la séquence suivante : rouge, bleu, vert, violet, orange, turquoise, gris. Ces couleurs se succèdent à nouveau pour chaque autre réviseur.</span><span class="sxs-lookup"><span data-stu-id="60ff0-p101">Colors are assigned to reviewers in the following sequence: red, blue, green, violet, orange, turquoise, gray. These colors are cycled through again for any remaining reviewers.</span></span> 
  
<span data-ttu-id="60ff0-108">Les commentaires entrés sur la page de dessin d'origine sont toujours de couleur jaune, peu importe la couleur attribuée à un réviseur dans la cellule Color.</span><span class="sxs-lookup"><span data-stu-id="60ff0-108">Comments entered on the original drawing page are always colored yellow, regardless of the color assigned to a reviewer in the Color cell.</span></span> 
  
<span data-ttu-id="60ff0-109">Pour obtenir une référence à la cellule Color par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="60ff0-109">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60ff0-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="60ff0-110">Cell name:</span></span>  <br/> | <span data-ttu-id="60ff0-111">Reviewer.Color [  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="60ff0-111">Reviewer.Color [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="60ff0-112">Pour obtenir une référence à la cellule Color à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="60ff0-112">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60ff0-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="60ff0-113">Section index:</span></span>  <br/> |<span data-ttu-id="60ff0-114">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="60ff0-114">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="60ff0-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="60ff0-115">Row index:</span></span>  <br/> |<span data-ttu-id="60ff0-116">**visRowReviewer**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="60ff0-116">**visRowReviewer** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="60ff0-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="60ff0-117">Cell index:</span></span>  <br/> |<span data-ttu-id="60ff0-118">**visReviewerColor**</span><span class="sxs-lookup"><span data-stu-id="60ff0-118">**visReviewerColor**</span></span> <br/> |
   

