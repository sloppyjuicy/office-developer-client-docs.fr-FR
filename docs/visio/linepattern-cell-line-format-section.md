---
title: LinePattern, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Détermine le motif de trait d'une forme. La valeur entrée dans la cellule LinePattern est un nombre correspondant à un index d'un ensemble de motifs de trait.
ms.openlocfilehash: cccc6028de21299942e62c53aba48622baa95f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788954"
---
# <a name="linepattern-cell-line-format-section"></a><span data-ttu-id="bee94-104">LinePattern, cellule (section Line Format)</span><span class="sxs-lookup"><span data-stu-id="bee94-104">LinePattern Cell (Line Format Section)</span></span>

<span data-ttu-id="bee94-p102">Détermine le motif de trait d'une forme. La valeur entrée dans la cellule LinePattern est un nombre correspondant à un index d'un ensemble de motifs de trait.</span><span class="sxs-lookup"><span data-stu-id="bee94-p102">Determines the line pattern of the shape. The value entered in the LinePattern cell is a number that is an index into a collection of line patterns.</span></span>
  
|<span data-ttu-id="bee94-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="bee94-107">**Value**</span></span>|<span data-ttu-id="bee94-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="bee94-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bee94-109">0</span><span class="sxs-lookup"><span data-stu-id="bee94-109">0</span></span>  <br/> |<span data-ttu-id="bee94-110">Aucun motif de trait</span><span class="sxs-lookup"><span data-stu-id="bee94-110">No line pattern</span></span>  <br/> |
|<span data-ttu-id="bee94-111">1</span><span class="sxs-lookup"><span data-stu-id="bee94-111">1</span></span>  <br/> |<span data-ttu-id="bee94-112">Uni</span><span class="sxs-lookup"><span data-stu-id="bee94-112">Solid</span></span>  <br/> |
|<span data-ttu-id="bee94-113">2 - 23</span><span class="sxs-lookup"><span data-stu-id="bee94-113">2 - 23</span></span>  <br/> |<span data-ttu-id="bee94-114">Motifs de trait assortis</span><span class="sxs-lookup"><span data-stu-id="bee94-114">Assorted line patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bee94-115">Note</span><span class="sxs-lookup"><span data-stu-id="bee94-115">Remarks</span></span>

<span data-ttu-id="bee94-116">Vous pouvez afficher l’ensemble des motifs de trait dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **tirets**, puis cliquez sur **Autres traits**).</span><span class="sxs-lookup"><span data-stu-id="bee94-116">You can view the line pattern collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Dashes**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="bee94-117">Pour choisir un motif de trait personnalisé, utilisez la fonction USE dans cette cellule.</span><span class="sxs-lookup"><span data-stu-id="bee94-117">To specify a custom line pattern, use the USE function in this cell.</span></span>
  
<span data-ttu-id="bee94-118">Pour obtenir une référence à la cellule LinePattern par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="bee94-118">To get a reference to the LinePattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bee94-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bee94-119">Cell name:</span></span>  <br/> |<span data-ttu-id="bee94-120">LinePattern</span><span class="sxs-lookup"><span data-stu-id="bee94-120">LinePattern</span></span>  <br/> |
   
<span data-ttu-id="bee94-121">Pour obtenir une référence à la cellule LinePattern par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bee94-121">To get a reference to the LinePattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bee94-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bee94-122">Section index:</span></span>  <br/> |<span data-ttu-id="bee94-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bee94-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bee94-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bee94-124">Row index:</span></span>  <br/> |<span data-ttu-id="bee94-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="bee94-125">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="bee94-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bee94-126">Cell index:</span></span>  <br/> |<span data-ttu-id="bee94-127">**visLinePattern**</span><span class="sxs-lookup"><span data-stu-id="bee94-127">**visLinePattern**</span></span> <br/> |
   

