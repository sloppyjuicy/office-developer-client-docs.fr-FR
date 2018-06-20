---
title: LineColor, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Détermine la couleur de trait de la forme.
ms.openlocfilehash: 6086a45108b88475e250c4d833ab4b740f33b8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788951"
---
# <a name="linecolor-cell-line-format-section"></a><span data-ttu-id="44005-103">LineColor, cellule (section Line Format)</span><span class="sxs-lookup"><span data-stu-id="44005-103">LineColor Cell (Line Format Section)</span></span>

<span data-ttu-id="44005-104">Détermine la couleur de trait de la forme.</span><span class="sxs-lookup"><span data-stu-id="44005-104">Determines the line color of the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44005-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="44005-105">Remarks</span></span>

<span data-ttu-id="44005-106">Pour définir la couleur de trait, entrez un nombre entre 0 et 23, qui est un index dans une collection de couleurs.</span><span class="sxs-lookup"><span data-stu-id="44005-106">To set the line color, enter a number from 0 to 23, which is an index into a collection of line colors.</span></span> <span data-ttu-id="44005-107">Vous pouvez afficher l’ensemble de couleur de trait dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **poids**, puis cliquez sur **Autres traits**).</span><span class="sxs-lookup"><span data-stu-id="44005-107">You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span> <span data-ttu-id="44005-108">Vous pouvez également définir la valeur de LineColor dans la boîte de dialogue **trait** .</span><span class="sxs-lookup"><span data-stu-id="44005-108">You can also set the value of LineColor in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="44005-109">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL.</span><span class="sxs-lookup"><span data-stu-id="44005-109">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="44005-110">La valeur d’une couleur personnalisée est sa couleur RVB et RVB ( *r, g, b*), au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="44005-110">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="44005-111">Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 24 et au-dessus.</span><span class="sxs-lookup"><span data-stu-id="44005-111">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="44005-112">Vous pouvez définir la transparence de la couleur du trait dans la cellule LineColorTrans.</span><span class="sxs-lookup"><span data-stu-id="44005-112">You can set the transparency of the line color in the LineColorTrans cell.</span></span>
  
<span data-ttu-id="44005-113">Pour obtenir une référence à la cellule LineColor par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="44005-113">To get a reference to the LineColor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44005-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="44005-114">Cell name:</span></span>  <br/> |<span data-ttu-id="44005-115">LineColor</span><span class="sxs-lookup"><span data-stu-id="44005-115">LineColor</span></span>  <br/> |
   
<span data-ttu-id="44005-116">Pour obtenir une référence à la cellule LineColor par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="44005-116">To get a reference to the LineColor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44005-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="44005-117">Section index:</span></span>  <br/> |<span data-ttu-id="44005-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="44005-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="44005-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="44005-119">Row index:</span></span>  <br/> |<span data-ttu-id="44005-120">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="44005-120">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="44005-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="44005-121">Cell index:</span></span>  <br/> |<span data-ttu-id="44005-122">**visLineColor**</span><span class="sxs-lookup"><span data-stu-id="44005-122">**visLineColor**</span></span> <br/> |
   

