---
title: DoubleULine, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Détermine si la plage de texte est soulignée ou non d'une ligne double.
ms.openlocfilehash: 2708e7f55e1fd04d5fb902b3d382035790cbbcc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357462"
---
# <a name="doubleuline-cell-character-section"></a><span data-ttu-id="ef885-103">DoubleULine, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="ef885-103">DoubleULine Cell (Character Section)</span></span>

<span data-ttu-id="ef885-104">Détermine si la plage de texte est soulignée ou non d'une ligne double.</span><span class="sxs-lookup"><span data-stu-id="ef885-104">Determines whether the range of text has a double underline below it.</span></span>
  
|<span data-ttu-id="ef885-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="ef885-105">**Value**</span></span>|<span data-ttu-id="ef885-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="ef885-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef885-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ef885-107">TRUE</span></span>  <br/> |<span data-ttu-id="ef885-108">Le texte est souligné en double.</span><span class="sxs-lookup"><span data-stu-id="ef885-108">Text has a double underline below it.</span></span>  <br/> |
|<span data-ttu-id="ef885-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ef885-109">FALSE</span></span>  <br/> |<span data-ttu-id="ef885-110">Le texte n'est pas souligné en double.</span><span class="sxs-lookup"><span data-stu-id="ef885-110">Text does not have a double underline below it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef885-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="ef885-111">Remarks</span></span>

<span data-ttu-id="ef885-p101">La cellule DoubleULine contient des informations de mise en forme qui s'appliquent à une plage du texte de la forme si la section Character contient plusieurs lignes ou à l'ensemble du texte dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ef885-p101">The DoubleULine cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="ef885-114">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (cliquez sur la flèche **Police** sous l’onglet **Accueil**).</span><span class="sxs-lookup"><span data-stu-id="ef885-114">You can also set the value of this cell by using the **Text** dialog box (click the **Font** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="ef885-115">Pour obtenir une référence à la cellule DoubleULine par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ef885-115">To get a reference to the DoubleULine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef885-116">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="ef885-116">Cell name:</span></span>  <br/> |<span data-ttu-id="ef885-117">Char. DblUnderline [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ef885-117">Char.DblUnderline[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ef885-118">Pour obtenir une référence à la cellule DoubleULine à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ef885-118">To get a reference to the DoubleULine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef885-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ef885-119">Section index:</span></span>  <br/> |<span data-ttu-id="ef885-120">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="ef885-120">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="ef885-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ef885-121">Row index:</span></span>  <br/> |<span data-ttu-id="ef885-122">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ef885-122">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="ef885-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ef885-123">Cell index:</span></span>  <br/> |<span data-ttu-id="ef885-124">**visCharacterDblUnderline**</span><span class="sxs-lookup"><span data-stu-id="ef885-124">**visCharacterDblUnderline**</span></span> <br/> |
   

