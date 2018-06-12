---
title: LineColorTrans, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
localization_priority: Normal
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: Détermine le niveau de transparence de la couleur de trait d'une forme.
ms.openlocfilehash: 81c23b77c4663158819f9d5fe53765860183e039
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788948"
---
# <a name="linecolortrans-cell-line-format-section"></a><span data-ttu-id="8bc2a-103">LineColorTrans, cellule (section Line Format)</span><span class="sxs-lookup"><span data-stu-id="8bc2a-103">LineColorTrans Cell (Line Format Section)</span></span>

<span data-ttu-id="8bc2a-104">Détermine le niveau de transparence de la couleur de trait d'une forme.</span><span class="sxs-lookup"><span data-stu-id="8bc2a-104">Determines the transparency level of a shape's line color.</span></span>
  
|<span data-ttu-id="8bc2a-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="8bc2a-105">**Value**</span></span>|<span data-ttu-id="8bc2a-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="8bc2a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8bc2a-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="8bc2a-107">0 - 100</span></span>  <br/> |<span data-ttu-id="8bc2a-p101">Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="8bc2a-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bc2a-110">Note</span><span class="sxs-lookup"><span data-stu-id="8bc2a-110">Remarks</span></span>

<span data-ttu-id="8bc2a-p102">Les valeurs sont arrondies au pourcentage le plus proche. Une valeur de 100 % correspond à une transparence totale. Même si une forme dont la couleur de trait est entièrement transparente apparaît identique à une forme dépourvue de traits sur la page de dessin, elle interagit avec les autres objets de la page de la même façon que si elle avait une transparence de 0 %.</span><span class="sxs-lookup"><span data-stu-id="8bc2a-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent line color appears the same as a shape with no lines on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span> 
  
<span data-ttu-id="8bc2a-114">Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **poids**, puis cliquez sur **Autres traits**).</span><span class="sxs-lookup"><span data-stu-id="8bc2a-114">You can also set this value by using the slider control in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="8bc2a-115">Pour obtenir une référence à la cellule LineColorTrans par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="8bc2a-115">To get a reference to the LineColorTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bc2a-116">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8bc2a-116">Cell name:</span></span>  <br/> |<span data-ttu-id="8bc2a-117">LineColorTrans</span><span class="sxs-lookup"><span data-stu-id="8bc2a-117">LineColorTrans</span></span>  <br/> |
   
<span data-ttu-id="8bc2a-118">Pour obtenir une référence à la cellule LineColorTrans par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8bc2a-118">To get a reference to the LineColorTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8bc2a-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8bc2a-119">Section index:</span></span>  <br/> |<span data-ttu-id="8bc2a-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8bc2a-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8bc2a-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8bc2a-121">Row index:</span></span>  <br/> |<span data-ttu-id="8bc2a-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="8bc2a-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="8bc2a-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8bc2a-123">Cell index:</span></span>  <br/> |<span data-ttu-id="8bc2a-124">**visLineColorTrans**</span><span class="sxs-lookup"><span data-stu-id="8bc2a-124">**visLineColorTrans**</span></span> <br/> |
   

