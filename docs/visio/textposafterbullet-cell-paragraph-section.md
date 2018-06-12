---
title: TextPosAfterBullet, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Représente la distance entre la première ligne du paragraphe et la puce.
ms.openlocfilehash: fe22b81113ab6537922ad4627aa53f34f2e62c48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789877"
---
# <a name="textposafterbullet-cell-paragraph-section"></a><span data-ttu-id="b6e00-103">TextPosAfterBullet, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="b6e00-103">TextPosAfterBullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="b6e00-104">Représente la distance entre la première ligne du paragraphe et la puce.</span><span class="sxs-lookup"><span data-stu-id="b6e00-104">Represents the distance between the first line of the paragraph and the bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b6e00-105">Note</span><span class="sxs-lookup"><span data-stu-id="b6e00-105">Remarks</span></span>

<span data-ttu-id="b6e00-p101">Cette distance est ajoutée à celle contenue dans la cellule IndFirst, qui est le retrait gauche par défaut. Cette valeur est indépendante de l'échelle du dessin.</span><span class="sxs-lookup"><span data-stu-id="b6e00-p101">This distance is added to the distance contained in the IndFirst cell, which is the default left indent. This value is independent of the scale of the drawing.</span></span> 
  
<span data-ttu-id="b6e00-108">Pour obtenir une référence à la cellule TextPosAfterBullet par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="b6e00-108">To get a reference to the TextPosAfterBullet cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6e00-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b6e00-109">Cell name:</span></span>  <br/> | <span data-ttu-id="b6e00-110">Para.TextPosAfterBullet [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b6e00-110">Para.TextPosAfterBullet[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b6e00-111">Pour obtenir une référence à la cellule TextPosAfterBullet par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b6e00-111">To get a reference to the TextPosAfterBullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6e00-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b6e00-112">Section index:</span></span>  <br/> |<span data-ttu-id="b6e00-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="b6e00-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="b6e00-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b6e00-114">Row index:</span></span>  <br/> |<span data-ttu-id="b6e00-115">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b6e00-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b6e00-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b6e00-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b6e00-117">**visTextPosAfterBullet**</span><span class="sxs-lookup"><span data-stu-id="b6e00-117">**visTextPosAfterBullet**</span></span> <br/> |
   

