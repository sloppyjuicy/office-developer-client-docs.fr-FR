---
title: Cellule XGridSpacing (règle &amp; Section grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Précise la distance entre les lignes horizontales dans une grille fixe (XGridDensity = 0).
ms.openlocfilehash: 5f461d02dae1574fe2b186b43166ef14d8251df2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790057"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a><span data-ttu-id="a7446-103">Cellule XGridSpacing (règle &amp; Section grille)</span><span class="sxs-lookup"><span data-stu-id="a7446-103">XGridSpacing Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="a7446-104">Précise la distance entre les lignes horizontales dans une grille fixe (XGridDensity = 0).</span><span class="sxs-lookup"><span data-stu-id="a7446-104">Specifies the distance between horizontal lines in a fixed grid (XGridDensity = 0).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7446-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7446-105">Remarks</span></span>

<span data-ttu-id="a7446-106">Cette cellule correspond à l' **Espacement minimal** horizontal d’option dans le **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ).</span><span class="sxs-lookup"><span data-stu-id="a7446-106">This cell corresponds to the horizontal **Minimum spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="a7446-107">Pour obtenir une référence à la cellule XGridSpacing par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="a7446-107">To get a reference to the XGridSpacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7446-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a7446-108">Cell name:</span></span>  <br/> |<span data-ttu-id="a7446-109">XGridSpacing</span><span class="sxs-lookup"><span data-stu-id="a7446-109">XGridSpacing</span></span>  <br/> |
   
<span data-ttu-id="a7446-110">Pour obtenir une référence à la cellule XGridSpacing par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a7446-110">To get a reference to the XGridSpacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7446-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a7446-111">Section index:</span></span>  <br/> |<span data-ttu-id="a7446-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a7446-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a7446-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a7446-113">Row index:</span></span>  <br/> |<span data-ttu-id="a7446-114">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="a7446-114">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="a7446-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a7446-115">Cell index:</span></span>  <br/> |<span data-ttu-id="a7446-116">**visXGridSpacing**</span><span class="sxs-lookup"><span data-stu-id="a7446-116">**visXGridSpacing**</span></span> <br/> |
   

