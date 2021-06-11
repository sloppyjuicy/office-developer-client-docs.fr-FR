---
title: Scale, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm870
localization_priority: Normal
ms.assetid: d6fe2574-b719-f38e-b1f1-592a812f1682
description: Contrôle la largeur de la police. La valeur par défaut de cette cellule est 100 %.
ms.openlocfilehash: 60e896772ddd1d59e1a1da7f2c0e90893658c624
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429151"
---
# <a name="scale-cell-character-section"></a><span data-ttu-id="9cc3c-104">Scale, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="9cc3c-104">Scale Cell (Character Section)</span></span>

<span data-ttu-id="9cc3c-p102">Contrôle la largeur de la police. La valeur par défaut de cette cellule est 100 %.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-p102">Controls the font width. The default value for this cell is 100%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9cc3c-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="9cc3c-107">Remarks</span></span>

<span data-ttu-id="9cc3c-p103">Donnez une valeur comprise entre 1 et 99 % pour réduire la largeur de la police. Donnez une valeur entre 101 et 600 % pour augmenter la largeur de la police.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-p103">Set the percentage between 1% and 99% to decrease the font width. Set it between 101% and 600% to increase the font width.</span></span>
  
<span data-ttu-id="9cc3c-110">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**).</span><span class="sxs-lookup"><span data-stu-id="9cc3c-110">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="9cc3c-111">Pour obtenir une référence à la cellule Scale par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9cc3c-111">To get a reference to the Scale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9cc3c-112">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="9cc3c-112">Cell name:</span></span>  <br/> |<span data-ttu-id="9cc3c-113">Char.FontScale[ *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9cc3c-113">Char.FontScale[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9cc3c-114">Pour obtenir une référence à la cellule Scale à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9cc3c-114">To get a reference to the Scale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9cc3c-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9cc3c-115">Section index:</span></span>  <br/> |<span data-ttu-id="9cc3c-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="9cc3c-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="9cc3c-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9cc3c-117">Row index:</span></span>  <br/> |<span data-ttu-id="9cc3c-118">**visRowCharacter**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9cc3c-118">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9cc3c-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9cc3c-119">Cell index:</span></span>  <br/> |<span data-ttu-id="9cc3c-120">**visCharacterFontScale**</span><span class="sxs-lookup"><span data-stu-id="9cc3c-120">**visCharacterFontScale**</span></span> <br/> |
   

