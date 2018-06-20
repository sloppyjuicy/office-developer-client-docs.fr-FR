---
title: LineWeight, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Détermine l’épaisseur d’un trait. Pour définir l’épaisseur, entrez un nombre accompagné d’une unité de mesure valide.
ms.openlocfilehash: a5207607d90ef6a79dcb3acc191521b73e2cdf54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788962"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="e43a5-104">LineWeight, cellule (section Line Format)</span><span class="sxs-lookup"><span data-stu-id="e43a5-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="e43a5-p102">Détermine l’épaisseur d’un trait. Pour définir l’épaisseur, entrez un nombre accompagné d’une unité de mesure valide.</span><span class="sxs-lookup"><span data-stu-id="e43a5-p102">Determines the line weight of a shape. Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e43a5-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="e43a5-107">Remarks</span></span>

<span data-ttu-id="e43a5-108">Vous pouvez également définir la valeur de LineWeight dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **poids**, puis cliquez sur **Autres traits**).</span><span class="sxs-lookup"><span data-stu-id="e43a5-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="e43a5-109">Si l’unité de mesure n’est pas entrée, l’unité de mesure pour le texte spécifié dans la boîte de dialogue **Options Visio** est utilisée (cliquez sur l’onglet **fichier** , puis cliquez sur **Options**).</span><span class="sxs-lookup"><span data-stu-id="e43a5-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="e43a5-110">Épaisseur de trait est indépendante de l’échelle du dessin.</span><span class="sxs-lookup"><span data-stu-id="e43a5-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="e43a5-111">Si le dessin est mis à l’échelle, l’épaisseur de trait reste identique.</span><span class="sxs-lookup"><span data-stu-id="e43a5-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="e43a5-112">Pour obtenir une référence à la cellule LineWeight par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="e43a5-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e43a5-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e43a5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e43a5-114">Épaisseur de trait</span><span class="sxs-lookup"><span data-stu-id="e43a5-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="e43a5-115">Pour obtenir une référence à la cellule LineWeight par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e43a5-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e43a5-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e43a5-116">Section index:</span></span>  <br/> |<span data-ttu-id="e43a5-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e43a5-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e43a5-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e43a5-118">Row index:</span></span>  <br/> |<span data-ttu-id="e43a5-119">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="e43a5-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="e43a5-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e43a5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e43a5-121">**visLineWeight**</span><span class="sxs-lookup"><span data-stu-id="e43a5-121">**visLineWeight**</span></span> <br/> |
   

