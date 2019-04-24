---
title: FillForegndTrans, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253231
localization_priority: Normal
ms.assetid: 8b1b3904-6635-3fd1-31a9-ff32c19394af
description: Détermine le degré de transparence de la couleur de premier plan dans le motif de remplissage de la forme.
ms.openlocfilehash: d05a83f83ea3d95ac3d42a2bfb3996917119f580
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322448"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a><span data-ttu-id="6756e-103">FillForegndTrans, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="6756e-103">FillForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="6756e-104">Détermine le degré de transparence de la couleur de premier plan dans le motif de remplissage de la forme.</span><span class="sxs-lookup"><span data-stu-id="6756e-104">Determines the transparency level for the foreground (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="6756e-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="6756e-105">**Value**</span></span>|<span data-ttu-id="6756e-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="6756e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6756e-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="6756e-107">0 - 100</span></span>  <br/> |<span data-ttu-id="6756e-p101">Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="6756e-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6756e-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="6756e-110">Remarks</span></span>

<span data-ttu-id="6756e-p102">Les valeurs sont arrondies au demi-point le plus proche. Une valeur de 100 % est complètement transparente. Bien qu'une forme au remplissage complètement transparent apparaisse sur la page de dessin comme une forme sans remplissage, ses effets sur les autres objets de la page seront les mêmes que si elle était complètement opaque.</span><span class="sxs-lookup"><span data-stu-id="6756e-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="6756e-p103">Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Remplissage** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Remplissage**, puis cliquez sur **Options de remplissage**). Cette valeur contrôle à la fois les transparences de l’ombre de l’arrière-plan et du premier plan. Pour les définir de façon indépendante, vous devez les entrer dans la fenêtre Feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6756e-p103">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**). This value controls the value of both the background and foreground fill transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="6756e-117">Pour obtenir une référence à la cellule FillForegndTrans par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="6756e-117">To get a reference to the FillForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6756e-118">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6756e-118">Cell name:</span></span>  <br/> |<span data-ttu-id="6756e-119">FillForegndTrans</span><span class="sxs-lookup"><span data-stu-id="6756e-119">FillForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="6756e-120">Pour obtenir une référence à la cellule FillForegndTrans à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="6756e-120">To get a reference to the FillForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6756e-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6756e-121">Section index:</span></span>  <br/> |<span data-ttu-id="6756e-122">**Définis**</span><span class="sxs-lookup"><span data-stu-id="6756e-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6756e-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6756e-123">Row index:</span></span>  <br/> |<span data-ttu-id="6756e-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="6756e-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="6756e-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6756e-125">Cell index:</span></span>  <br/> |<span data-ttu-id="6756e-126">**visFillForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="6756e-126">**visFillForegndTrans**</span></span> <br/> |
   

