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
ms.openlocfilehash: d9182932b8fa63c30473b93e420aa9efe30bf5eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438665"
---
# <a name="font-cell-character-section"></a><span data-ttu-id="0998f-105">Font, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="0998f-105">Font Cell (Character Section)</span></span>

<span data-ttu-id="0998f-p102">Représente le numéro de la police utilisée pour mettre le texte en forme. Ce numéro dépend des polices installées sur votre système. 0 représente la police par défaut, généralement Arial.</span><span class="sxs-lookup"><span data-stu-id="0998f-p102">Represents the number of the font used to format the text. Font numbers vary according to the fonts installed on your system. The number 0 represents the default font, which is typically Arial.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0998f-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="0998f-109">Remarks</span></span>

<span data-ttu-id="0998f-110">Pour obtenir une référence à la cellule Font par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="0998f-110">To get a reference to the Font cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0998f-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0998f-111">Cell name:</span></span>  <br/> | <span data-ttu-id="0998f-112">Char.Font[  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0998f-112">Char.Font[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0998f-113">Pour obtenir une référence à la cellule Font à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="0998f-113">To get a reference to the Font cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0998f-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="0998f-114">Section index:</span></span>  <br/> |<span data-ttu-id="0998f-115">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="0998f-115">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="0998f-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="0998f-116">Row index:</span></span>  <br/> |<span data-ttu-id="0998f-117">**visRowCharacter**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0998f-117">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0998f-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0998f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="0998f-119">**visCharacterFont**</span><span class="sxs-lookup"><span data-stu-id="0998f-119">**visCharacterFont**</span></span> <br/> |
   

