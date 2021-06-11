---
title: TextBkgndTrans, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: Détermine le niveau de transparence de la couleur d'arrière-plan du bloc de texte de la forme.
ms.openlocfilehash: f4c4dc7700c553bd4c9bee337220e357c4c5538a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408690"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a><span data-ttu-id="6480f-103">TextBkgndTrans, cellule (section Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="6480f-103">TextBkgndTrans Cell (Text Block Format Section)</span></span>

<span data-ttu-id="6480f-104">Détermine le niveau de transparence de la couleur d'arrière-plan du bloc de texte de la forme.</span><span class="sxs-lookup"><span data-stu-id="6480f-104">Determines the transparency level for the background color of the shape's text block.</span></span>
  
|<span data-ttu-id="6480f-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="6480f-105">**Value**</span></span>|<span data-ttu-id="6480f-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="6480f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6480f-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="6480f-107">0 - 100</span></span>  <br/> |<span data-ttu-id="6480f-p101">Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="6480f-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6480f-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="6480f-110">Remarks</span></span>

<span data-ttu-id="6480f-p102">Les valeurs sont arrondies au pourcentage le plus proche. Une valeur de 100 % correspond à une transparence totale. Même si une forme dont l’arrière-plan de texte est entièrement transparent apparaît identique sur la page de dessin à une forme dépourvue d’arrière-plan de texte, elle interagit avec les autres objets de la page de la même façon que si elle avait une transparence de 0 %.</span><span class="sxs-lookup"><span data-stu-id="6480f-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape that has a completely transparent text background appears the same on the drawing page as a shape that has no text background, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="6480f-114">Vous pouvez également définir cette valeur à l’aide du curseur sous l’onglet **Police** de la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**).</span><span class="sxs-lookup"><span data-stu-id="6480f-114">You can also set this value using the slider control on the **Font** tab of the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="6480f-115">Pour obtenir une référence à la cellule TextBkgndTrans par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="6480f-115">To get a reference to the TextBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6480f-116">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="6480f-116">Cell name:</span></span>  <br/> |<span data-ttu-id="6480f-117">TextBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="6480f-117">TextBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="6480f-118">Pour obtenir une référence à la cellule TextBkgndTrans par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="6480f-118">To get a reference to the TextBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6480f-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6480f-119">Section index:</span></span>  <br/> |<span data-ttu-id="6480f-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6480f-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6480f-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6480f-121">Row index:</span></span>  <br/> |<span data-ttu-id="6480f-122">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="6480f-122">**visRowText**</span></span> <br/> |
|<span data-ttu-id="6480f-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6480f-123">Cell index:</span></span>  <br/> |<span data-ttu-id="6480f-124">**visTxtBlkBkgndTrans**</span><span class="sxs-lookup"><span data-stu-id="6480f-124">**visTxtBlkBkgndTrans**</span></span> <br/> |
   

