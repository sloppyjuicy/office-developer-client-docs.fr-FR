---
title: XGridSpacing, cellule (section Ruler &amp; Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Précise la distance entre les lignes horizontales dans une grille fixe (XGridDensity = 0).
ms.openlocfilehash: 05b68a9721dbfc9c03402d384d976c42ef05b134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435074"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="ec51f-103">XGridSpacing, cellule (section Ruler &amp; Grid)</span><span class="sxs-lookup"><span data-stu-id="ec51f-103">XGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="ec51f-104">Précise la distance entre les lignes horizontales dans une grille fixe (XGridDensity = 0).</span><span class="sxs-lookup"><span data-stu-id="ec51f-104">Specifies the distance between horizontal lines in a fixed grid (XGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec51f-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="ec51f-105">Remarks</span></span>

<span data-ttu-id="ec51f-106">Cette cellule correspond à l’option d’espacement **minimal** horizontal  dans la boîte de dialogue Grille de règle (sous l’onglet Affichage, cliquez sur **Afficher** la flèche). **&amp;**</span><span class="sxs-lookup"><span data-stu-id="ec51f-106">This cell corresponds to the horizontal **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="ec51f-107">Pour obtenir une référence à la cellule XGridSpacing par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ec51f-107">To get a reference to the XGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ec51f-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ec51f-108">Cell name:</span></span>  <br/> |<span data-ttu-id="ec51f-109">XGridSpacing</span><span class="sxs-lookup"><span data-stu-id="ec51f-109">XGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="ec51f-110">Pour obtenir une référence à la cellule XGridSpacing par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ec51f-110">To get a reference to the XGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ec51f-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ec51f-111">Section index:</span></span>  <br/> |<span data-ttu-id="ec51f-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ec51f-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ec51f-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ec51f-113">Row index:</span></span>  <br/> |<span data-ttu-id="ec51f-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="ec51f-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="ec51f-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ec51f-115">Cell index:</span></span>  <br/> |<span data-ttu-id="ec51f-116">**visXGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="ec51f-116">**visXGridSpacing**</span></span> <br/> |
   

