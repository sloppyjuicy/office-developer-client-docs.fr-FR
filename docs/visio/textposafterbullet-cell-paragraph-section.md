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
ms.openlocfilehash: a98967cb5f9541434745c3b3d6afafde0878074a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422151"
---
# <a name="textposafterbullet-cell-paragraph-section"></a><span data-ttu-id="1b783-103">TextPosAfterBullet, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="1b783-103">TextPosAfterBullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="1b783-104">Représente la distance entre la première ligne du paragraphe et la puce.</span><span class="sxs-lookup"><span data-stu-id="1b783-104">Represents the distance between the first line of the paragraph and the bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1b783-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="1b783-105">Remarks</span></span>

<span data-ttu-id="1b783-p101">Cette distance est ajoutée à celle contenue dans la cellule IndFirst, qui est le retrait gauche par défaut. Cette valeur est indépendante de l'échelle du dessin.</span><span class="sxs-lookup"><span data-stu-id="1b783-p101">This distance is added to the distance contained in the IndFirst cell, which is the default left indent. This value is independent of the scale of the drawing.</span></span> 
  
<span data-ttu-id="1b783-108">Pour obtenir une référence à la cellule TextPosAfterBullet à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="1b783-108">To get a reference to the TextPosAfterBullet cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1b783-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1b783-109">Cell name:</span></span>  <br/> | <span data-ttu-id="1b783-110">Para.TextPosAfterBullet[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1b783-110">Para.TextPosAfterBullet[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1b783-111">Pour obtenir une référence à la cellule TextPosAfterBullet à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1b783-111">To get a reference to the TextPosAfterBullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1b783-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1b783-112">Section index:</span></span>  <br/> |<span data-ttu-id="1b783-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="1b783-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="1b783-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1b783-114">Row index:</span></span>  <br/> |<span data-ttu-id="1b783-115">**visRowParagraph**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1b783-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1b783-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1b783-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1b783-117">**visTextPosAfterBullet**</span><span class="sxs-lookup"><span data-stu-id="1b783-117">**visTextPosAfterBullet**</span></span> <br/> |
   

