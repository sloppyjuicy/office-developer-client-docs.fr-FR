---
title: Spacing, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: Définit l'espace entre les caractères. Les espaces peuvent être ajoutés ou déduits par incréments de 1/20e de point.
ms.openlocfilehash: ee714306e22cafb7f6d805851a6f977e93172377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789798"
---
# <a name="spacing-cell-character-section"></a><span data-ttu-id="50815-104">Spacing, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="50815-104">Spacing Cell (Character Section)</span></span>

<span data-ttu-id="50815-p102">Définit l'espace entre les caractères. Les espaces peuvent être ajoutés ou déduits par incréments de 1/20e de point.</span><span class="sxs-lookup"><span data-stu-id="50815-p102">Controls the amount of space between two or more characters. Space can be added or subtracted in 1/20th point increments.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50815-107">Note</span><span class="sxs-lookup"><span data-stu-id="50815-107">Remarks</span></span>

<span data-ttu-id="50815-108">Vous pouvez également définir la valeur de cette cellule à l’aide de la boîte de dialogue **texte** (sous l’onglet **accueil** , cliquez sur la flèche **police** ).</span><span class="sxs-lookup"><span data-stu-id="50815-108">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="50815-109">Pour obtenir une référence à la cellule Spacing par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="50815-109">To get a reference to the Spacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50815-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="50815-110">Cell name:</span></span>  <br/> |<span data-ttu-id="50815-111">Char.Letterspace [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="50815-111">Char.Letterspace[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="50815-112">Pour obtenir une référence à la cellule Spacing par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="50815-112">To get a reference to the Spacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50815-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="50815-113">Section index:</span></span>  <br/> |<span data-ttu-id="50815-114">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="50815-114">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="50815-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="50815-115">Row index:</span></span>  <br/> |<span data-ttu-id="50815-116">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="50815-116">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="50815-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="50815-117">Cell index:</span></span>  <br/> |<span data-ttu-id="50815-118">**visCharacterLetterspace**</span><span class="sxs-lookup"><span data-stu-id="50815-118">**visCharacterLetterspace**</span></span> <br/> |
   

