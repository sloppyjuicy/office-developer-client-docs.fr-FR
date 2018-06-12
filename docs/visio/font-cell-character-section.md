---
title: Font, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Représente le numéro de la police utilisée pour mettre le texte en forme. Ce numéro dépend des polices installées sur votre système. 0 représente la police par défaut, généralement Arial.
ms.openlocfilehash: cbbf2a2400c995e0cbc217c1161fbd18f7459b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788656"
---
# <a name="font-cell-character-section"></a><span data-ttu-id="5ea10-105">Font, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="5ea10-105">Font Cell (Character Section)</span></span>

<span data-ttu-id="5ea10-p102">Représente le numéro de la police utilisée pour mettre le texte en forme. Ce numéro dépend des polices installées sur votre système. 0 représente la police par défaut, généralement Arial.</span><span class="sxs-lookup"><span data-stu-id="5ea10-p102">Represents the number of the font used to format the text. Font numbers vary according to the fonts installed on your system. The number 0 represents the default font, which is typically Arial.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ea10-109">Note</span><span class="sxs-lookup"><span data-stu-id="5ea10-109">Remarks</span></span>

<span data-ttu-id="5ea10-110">Pour obtenir une référence à la cellule Font par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="5ea10-110">To get a reference to the Font cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ea10-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5ea10-111">Cell name:</span></span>  <br/> | <span data-ttu-id="5ea10-112">Char.Font [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5ea10-112">Char.Font[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5ea10-113">Pour obtenir une référence à la cellule Font par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5ea10-113">To get a reference to the Font cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ea10-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5ea10-114">Section index:</span></span>  <br/> |<span data-ttu-id="5ea10-115">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="5ea10-115">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="5ea10-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5ea10-116">Row index:</span></span>  <br/> |<span data-ttu-id="5ea10-117">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5ea10-117">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5ea10-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5ea10-118">Cell index:</span></span>  <br/> |<span data-ttu-id="5ea10-119">**visCharacterFont**</span><span class="sxs-lookup"><span data-stu-id="5ea10-119">**visCharacterFont**</span></span> <br/> |
   

