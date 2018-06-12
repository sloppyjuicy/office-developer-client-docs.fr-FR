---
title: EndArrow, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Indique si un trait comporte une pointe de flèche ou un autre format d'extrémité de ligne à son dernier sommet.
ms.openlocfilehash: fa37e4896fdab0f2e8fee6d94aa38c72519a7e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788553"
---
# <a name="endarrow-cell-line-format-section"></a><span data-ttu-id="9b076-103">EndArrow, cellule (section Line Format)</span><span class="sxs-lookup"><span data-stu-id="9b076-103">EndArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="9b076-104">Indique si un trait comporte une pointe de flèche ou un autre format d'extrémité de ligne à son dernier sommet.</span><span class="sxs-lookup"><span data-stu-id="9b076-104">Indicates whether a line has an arrowhead or other line end format at its last vertex.</span></span>
  
|<span data-ttu-id="9b076-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9b076-105">**Value**</span></span>|<span data-ttu-id="9b076-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="9b076-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b076-107">0</span><span class="sxs-lookup"><span data-stu-id="9b076-107">0</span></span>  <br/> |<span data-ttu-id="9b076-108">Pas de pointe</span><span class="sxs-lookup"><span data-stu-id="9b076-108">No arrowhead.</span></span>  <br/> |
|<span data-ttu-id="9b076-109">1 - 45</span><span class="sxs-lookup"><span data-stu-id="9b076-109">1 - 45</span></span>  <br/> |<span data-ttu-id="9b076-110">Styles de pointes de flèches assortis correspondant aux entrées indexées de la boîte de dialogue **trait** .</span><span class="sxs-lookup"><span data-stu-id="9b076-110">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b076-111">Note</span><span class="sxs-lookup"><span data-stu-id="9b076-111">Remarks</span></span>

<span data-ttu-id="9b076-112">Vous pouvez également définir cette valeur dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **flèches**, puis cliquez sur **Autres flèches**).</span><span class="sxs-lookup"><span data-stu-id="9b076-112">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span> <span data-ttu-id="9b076-113">La taille de la pointe de flèche est définie dans la cellule EndArrowSize.</span><span class="sxs-lookup"><span data-stu-id="9b076-113">The size of the arrowhead is set in the EndArrowSize cell.</span></span>
  
<span data-ttu-id="9b076-114">Vous pouvez définir une extrémité de trait personnalisée à l'aide de la fonction USE dans cette cellule.</span><span class="sxs-lookup"><span data-stu-id="9b076-114">You can specify a custom line end using the USE function in this cell.</span></span> 
  
<span data-ttu-id="9b076-115">Pour obtenir une référence à la cellule EndArrow par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="9b076-115">To get a reference to the EndArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b076-116">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9b076-116">Cell name:</span></span>  <br/> |<span data-ttu-id="9b076-117">EndArrow</span><span class="sxs-lookup"><span data-stu-id="9b076-117">EndArrow</span></span>  <br/> |
   
<span data-ttu-id="9b076-118">Pour obtenir une référence à la cellule EndArrow par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9b076-118">To get a reference to the EndArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b076-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9b076-119">Section index:</span></span>  <br/> |<span data-ttu-id="9b076-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9b076-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9b076-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9b076-121">Row index:</span></span>  <br/> |<span data-ttu-id="9b076-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="9b076-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="9b076-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9b076-123">Cell index:</span></span>  <br/> |<span data-ttu-id="9b076-124">**visLineEndArrow**</span><span class="sxs-lookup"><span data-stu-id="9b076-124">**visLineEndArrow**</span></span> <br/> |
   

