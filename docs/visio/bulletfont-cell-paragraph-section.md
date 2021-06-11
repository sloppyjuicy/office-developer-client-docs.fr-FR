---
title: BulletFont, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Représente le numéro de la police utilisée pour mettre en forme le texte lorsqu'une chaîne de puces personnalisée est spécifiée et que la valeur dans la cellule Bullet est non nulle.
ms.openlocfilehash: 1cf04917bb7dfa68ee9395abb66ffe9e150f0273
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438462"
---
# <a name="bulletfont-cell-paragraph-section"></a><span data-ttu-id="578c8-103">BulletFont, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="578c8-103">BulletFont Cell (Paragraph Section)</span></span>

<span data-ttu-id="578c8-104">Représente le numéro de la police utilisée pour mettre en forme le texte lorsqu'une chaîne de puces personnalisée est spécifiée et que la valeur dans la cellule Bullet est non nulle.</span><span class="sxs-lookup"><span data-stu-id="578c8-104">Represents the number of the font used to format the text when a custom bullet string is specified and the value in the Bullet cell is non-zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="578c8-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="578c8-105">Remarks</span></span>

<span data-ttu-id="578c8-p101">Les numéros de police varient en fonction des polices installées sur votre système. Si la valeur est 0 et s'il y a une chaîne de puces personnalisée, la police utilisée est la même que la police du premier caractère du paragraphe.</span><span class="sxs-lookup"><span data-stu-id="578c8-p101">Font numbers vary according to the fonts installed on your system. If the value is 0 and there is a custom bullet string, the font used is the same as the font of the first character of the paragraph.</span></span>
  
<span data-ttu-id="578c8-108">Pour obtenir une référence à la cellule BulletFont par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="578c8-108">To get a reference to the BulletFont cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="578c8-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="578c8-109">Cell name:</span></span>  <br/> | <span data-ttu-id="578c8-110">Para.BulletFont[  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="578c8-110">Para.BulletFont[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="578c8-111">Pour obtenir une référence à la cellule BulletFont à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="578c8-111">To get a reference to the BulletFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="578c8-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="578c8-112">Section index:</span></span>  <br/> |<span data-ttu-id="578c8-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="578c8-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="578c8-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="578c8-114">Row index:</span></span>  <br/> |<span data-ttu-id="578c8-115">**visRowParagraph**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="578c8-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="578c8-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="578c8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="578c8-117">**visBulletFont**</span><span class="sxs-lookup"><span data-stu-id="578c8-117">**visBulletFont**</span></span> <br/> |
   

