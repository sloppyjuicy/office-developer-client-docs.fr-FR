---
title: Strikethru, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Détermine si le texte est barré.
ms.openlocfilehash: 4a58123814a4782c279a36d202e1293ec222ef93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412428"
---
# <a name="strikethru-cell-character-section"></a><span data-ttu-id="b3852-103">Strikethru, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="b3852-103">Strikethru Cell (Character Section)</span></span>

<span data-ttu-id="b3852-104">Détermine si le texte est barré.</span><span class="sxs-lookup"><span data-stu-id="b3852-104">Determines whether the text is formatted as strikethrough.</span></span>
  
|<span data-ttu-id="b3852-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b3852-105">**Value**</span></span>|<span data-ttu-id="b3852-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b3852-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b3852-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b3852-107">TRUE</span></span>  <br/> |<span data-ttu-id="b3852-108">Le texte est barré.</span><span class="sxs-lookup"><span data-stu-id="b3852-108">Text is formatted as strikethrough.</span></span>  <br/> |
|<span data-ttu-id="b3852-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b3852-109">FALSE</span></span>  <br/> |<span data-ttu-id="b3852-110">Le texte n'est pas barré.</span><span class="sxs-lookup"><span data-stu-id="b3852-110">Text is not formatted as strikethrough.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3852-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="b3852-111">Remarks</span></span>

<span data-ttu-id="b3852-112">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Texte** (sous l’onglet **Accueil**, cliquez sur la flèche **Police**).</span><span class="sxs-lookup"><span data-stu-id="b3852-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="b3852-113">Pour obtenir une référence à la cellule Strikethru par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b3852-113">To get a reference to the Strikethru cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3852-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="b3852-114">Cell name:</span></span>  <br/> |<span data-ttu-id="b3852-115">Char.Strikethru[ *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b3852-115">Char.Strikethru[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b3852-116">Pour obtenir une référence à la cellule Strikethru par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b3852-116">To get a reference to the Strikethru cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3852-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b3852-117">Section index:</span></span>  <br/> |<span data-ttu-id="b3852-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="b3852-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="b3852-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b3852-119">Row index:</span></span>  <br/> |<span data-ttu-id="b3852-120">**visRowCharacter**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b3852-120">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b3852-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b3852-121">Cell index:</span></span>  <br/> |<span data-ttu-id="b3852-122">**visCharacterStrikethru**</span><span class="sxs-lookup"><span data-stu-id="b3852-122">**visCharacterStrikethru**</span></span> <br/> |
   

