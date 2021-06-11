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
ms.openlocfilehash: d0b4ebee6d96bc67c9ca45e8a6194cb91ed6c7f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416936"
---
# <a name="linecolor-cell-line-format-section"></a><span data-ttu-id="d41cf-103">LineColor, cellule (section Line Format)</span><span class="sxs-lookup"><span data-stu-id="d41cf-103">LineColor Cell (Line Format Section)</span></span>

<span data-ttu-id="d41cf-104">Détermine la couleur de trait de la forme.</span><span class="sxs-lookup"><span data-stu-id="d41cf-104">Determines the line color of the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d41cf-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d41cf-105">Remarks</span></span>

<span data-ttu-id="d41cf-p101">Pour définir la couleur de trait, entrez un nombre compris entre 0 et 23. Il s’agit d’un index d’un ensemble de couleurs de trait. Vous pouvez afficher l’ensemble de couleurs de trait dans la boîte de dialogue **Trait** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Trait**, pointez sur **Poids**, puis cliquez sur **Autres traits**). Vous pouvez également définir la valeur de LineColor dans la boîte de dialogue **Trait**.</span><span class="sxs-lookup"><span data-stu-id="d41cf-p101">To set the line color, enter a number from 0 to 23, which is an index into a collection of line colors. You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**). You can also set the value of LineColor in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="d41cf-109">Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL.</span><span class="sxs-lookup"><span data-stu-id="d41cf-109">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="d41cf-110">La valeur d’une couleur personnalisée est sa couleur RVB, et RVB( *r, g, b*), plutôt qu’un nombre, s’affiche dans la fenêtre Feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="d41cf-110">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="d41cf-111">Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24.</span><span class="sxs-lookup"><span data-stu-id="d41cf-111">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="d41cf-112">Vous pouvez définir la transparence de la couleur du trait dans la cellule LineColorTrans.</span><span class="sxs-lookup"><span data-stu-id="d41cf-112">You can set the transparency of the line color in the LineColorTrans cell.</span></span>
  
<span data-ttu-id="d41cf-113">Pour obtenir une référence à la cellule LineColor par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d41cf-113">To get a reference to the LineColor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d41cf-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d41cf-114">Cell name:</span></span>  <br/> |<span data-ttu-id="d41cf-115">LineColor</span><span class="sxs-lookup"><span data-stu-id="d41cf-115">LineColor</span></span>  <br/> |
   
<span data-ttu-id="d41cf-116">Pour obtenir une référence à la cellule LineColor à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d41cf-116">To get a reference to the LineColor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d41cf-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d41cf-117">Section index:</span></span>  <br/> |<span data-ttu-id="d41cf-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d41cf-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d41cf-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d41cf-119">Row index:</span></span>  <br/> |<span data-ttu-id="d41cf-120">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="d41cf-120">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="d41cf-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d41cf-121">Cell index:</span></span>  <br/> |<span data-ttu-id="d41cf-122">**visLineColor**</span><span class="sxs-lookup"><span data-stu-id="d41cf-122">**visLineColor**</span></span> <br/> |
   

