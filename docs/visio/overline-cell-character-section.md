---
title: Overline, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Détermine si le texte est surmonté d'un trait.
ms.openlocfilehash: 3ceb0f5bcb6f66098938e49ea5f176921d0c9808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789192"
---
# <a name="overline-cell-character-section"></a><span data-ttu-id="4f365-103">Overline, cellule (section Character)</span><span class="sxs-lookup"><span data-stu-id="4f365-103">Overline Cell (Character Section)</span></span>

<span data-ttu-id="4f365-104">Détermine si le texte est surmonté d'un trait.</span><span class="sxs-lookup"><span data-stu-id="4f365-104">Determines whether the text has a line above it.</span></span>
  
|<span data-ttu-id="4f365-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4f365-105">**Value**</span></span>|<span data-ttu-id="4f365-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="4f365-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f365-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4f365-107">TRUE</span></span>  <br/> |<span data-ttu-id="4f365-108">Le texte est surmonté d'un trait.</span><span class="sxs-lookup"><span data-stu-id="4f365-108">Text has a line above it.</span></span>  <br/> |
|<span data-ttu-id="4f365-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4f365-109">FALSE</span></span>  <br/> |<span data-ttu-id="4f365-110">Le texte n'est pas surmonté d'un trait.</span><span class="sxs-lookup"><span data-stu-id="4f365-110">Text does not have a line above it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f365-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="4f365-111">Remarks</span></span>

<span data-ttu-id="4f365-112">Vous pouvez également définir la valeur de cette cellule à l’aide de la boîte de dialogue **texte** (sous l’onglet **accueil** , cliquez sur la flèche **police** ).</span><span class="sxs-lookup"><span data-stu-id="4f365-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="4f365-113">Pour obtenir une référence à la cellule Overline par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="4f365-113">To get a reference to the Overline cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f365-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4f365-114">Cell name:</span></span>  <br/> |<span data-ttu-id="4f365-115">Char.Overline [ *i* ] où *i* = < 1 >, 2.</span><span class="sxs-lookup"><span data-stu-id="4f365-115">Char.Overline[ *i*  ] where  *i*  = <1>, 2.</span></span> <span data-ttu-id="4f365-116">3...</span><span class="sxs-lookup"><span data-stu-id="4f365-116">3...</span></span>  <br/> |
   
<span data-ttu-id="4f365-117">Pour obtenir une référence à la cellule Overline par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="4f365-117">To get a reference to the Overline cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f365-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="4f365-118">Section index:</span></span>  <br/> |<span data-ttu-id="4f365-119">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="4f365-119">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="4f365-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="4f365-120">Row index:</span></span>  <br/> |<span data-ttu-id="4f365-121">**visRowCharacter** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4f365-121">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4f365-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4f365-122">Cell index:</span></span>  <br/> |<span data-ttu-id="4f365-123">**visCharacterOverline**</span><span class="sxs-lookup"><span data-stu-id="4f365-123">**visCharacterOverline**</span></span> <br/> |
   

