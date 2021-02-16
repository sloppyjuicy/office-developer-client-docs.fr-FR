---
title: Transparency, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Détermine le niveau de transparence d'une plage de la couleur de texte d'une forme.
ms.openlocfilehash: 8619ec25372ae163fff1759aca36ff6693820e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427835"
---
# <a name="transparency-cell-character-section"></a><span data-ttu-id="028f2-103">Transparency, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="028f2-103">Transparency Cell (Character Section)</span></span>

<span data-ttu-id="028f2-104">Détermine le niveau de transparence d'une plage de la couleur de texte d'une forme.</span><span class="sxs-lookup"><span data-stu-id="028f2-104">Determines the transparency level for a range of a shape's text color.</span></span>
  
|<span data-ttu-id="028f2-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="028f2-105">**Value**</span></span>|<span data-ttu-id="028f2-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="028f2-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="028f2-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="028f2-107">0 - 100</span></span>  <br/> |<span data-ttu-id="028f2-p101">Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="028f2-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="028f2-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="028f2-110">Remarks</span></span>

<span data-ttu-id="028f2-p102">Les valeurs sont arrondies au pourcentage le plus proche. Une valeur de 100 % correspond à une transparence totale. Même si une forme dont le texte est entièrement transparent apparaît identique sur la page de dessin à une forme dépourvue de texte, elle interagit avec les autres objets de la page de la même façon que si elle avait une transparence de 0 %.</span><span class="sxs-lookup"><span data-stu-id="028f2-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape that has completely transparent text appears the same on the drawing page as a shape that has no text, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="028f2-114">Vous pouvez également définir cette valeur à  l’aide du curseur sous  l’onglet Police de la boîte de dialogue Texte (sous l’onglet Accueil, cliquez sur la **flèche Police).** </span><span class="sxs-lookup"><span data-stu-id="028f2-114">You can also set this value by using the slider control on the **Font** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="028f2-p103">Si la section Characters contient plusieurs lignes, la cellule Transparency contient des informations de mise en forme qui sont appliquées à une sous-plage du texte d’une forme. Dans le cas contraire, elle contient des informations de mise en forme pour la totalité du texte de la forme.</span><span class="sxs-lookup"><span data-stu-id="028f2-p103">If the Characters section contains multiple rows, the Transparency cell contains formatting information applied to a sub-range of a shape's text. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="028f2-117">Pour obtenir une référence à la cellule Transparency par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="028f2-117">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="028f2-118">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="028f2-118">Cell name:</span></span>  <br/> |<span data-ttu-id="028f2-119">Char.ColorTrans[ *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="028f2-119">Char.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="028f2-120">Pour obtenir une référence à la cellule Transparency par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="028f2-120">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="028f2-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="028f2-121">Section index:</span></span>  <br/> |<span data-ttu-id="028f2-122">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="028f2-122">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="028f2-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="028f2-123">Row index:</span></span>  <br/> |<span data-ttu-id="028f2-124">**visRowCharacter**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="028f2-124">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="028f2-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="028f2-125">Cell index:</span></span>  <br/> |<span data-ttu-id="028f2-126">**visCharacterColorTrans**</span><span class="sxs-lookup"><span data-stu-id="028f2-126">**visCharacterColorTrans**</span></span> <br/> |
   

