---
title: DrawingScale, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm265
localization_priority: Normal
ms.assetid: bc447f22-a188-2c61-e33c-df0d401a4725
description: Représente la valeur de l'unité de dessin dans l'échelle de dessin en cours. L'échelle de dessin est le rapport entre l'unité de page représentée dans la cellule PageScale et l'unité de dessin représentée dans la cellule DrawingScale.
ms.openlocfilehash: 8a3a5f93ff096e42ba3c13b671b46bf1cf97df82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316505"
---
# <a name="drawingscale-cell-page-properties-section"></a><span data-ttu-id="bb778-104">DrawingScale, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="bb778-104">DrawingScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="bb778-p102">Représente la valeur de l'unité de dessin dans l'échelle de dessin en cours. L'échelle de dessin est le rapport entre l'unité de page représentée dans la cellule PageScale et l'unité de dessin représentée dans la cellule DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="bb778-p102">Represents the value of the drawing unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
<span data-ttu-id="bb778-107">Vous pouvez définir la cellule DrawingScale de manière à modifier les unités de la règle à partir d'un programme.</span><span class="sxs-lookup"><span data-stu-id="bb778-107">You can set the DrawingScale cell to change the units of a page's rulers from a program.</span></span> <span data-ttu-id="bb778-108">Voici un exemple qui montre comment changer en centimètres les unités exprimées en pouces à partir d'un programme.</span><span class="sxs-lookup"><span data-stu-id="bb778-108">Here is an example of changing the measurement units from inches to centimeters from a program.</span></span> <span data-ttu-id="bb778-109">Ici, nous utilisons la méthode **ConvertResult** pour conserver la même distance et l'exprimer dans une unité différente.</span><span class="sxs-lookup"><span data-stu-id="bb778-109">In this case, we use the **ConvertResult** method to keep the distance the same but express it in different units.</span></span> 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

<span data-ttu-id="bb778-110">Vous pouvez déterminer le système de mesure d'un dessin en examinant la propriété **Units** de la cellule DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="bb778-110">You can determine the measurement system in a drawing by examining the **Units** property of the DrawingScale cell.</span></span> <span data-ttu-id="bb778-111">Après avoir exécuté la macro ci-dessus, l'instruction suivante exécutée dans la fenêtre exécution de Visual Basic Editor renvoie la *valeur true* .</span><span class="sxs-lookup"><span data-stu-id="bb778-111">After running the above macro the following statement executed in the Visual Basic Editor Immediate window will return  *True*  .</span></span> 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a><span data-ttu-id="bb778-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb778-112">Remarks</span></span>

<span data-ttu-id="bb778-113">Cette cellule correspond aux paramètres de la boîte de dialogue **Mise en page** (cliquez sur la flèche **Mise en page** sous l’onglet **Accueil**).</span><span class="sxs-lookup"><span data-stu-id="bb778-113">This cell corresponds to the settings in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="bb778-p105">Les unités de la formule contenue dans la cellule DrawingScale définissent également les unités de mesure des règles dans la fenêtre de dessin. Si vous ne souhaitez pas modifier en même temps l'échelle du dessin, vous pouvez procéder de l'une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="bb778-p105">The units of the formula in the DrawingScale cell determine the measurement units used by the rulers in the drawing window. If you do not want to also change the drawing's scale, you can do one of the following:</span></span>
  
- <span data-ttu-id="bb778-116">conservez la distance indiquée dans la cellule DrawingScale, mais convertissez-la dans une unité différente ;</span><span class="sxs-lookup"><span data-stu-id="bb778-116">Keep the distance expressed in the DrawingScale cell the same but express it in different units.</span></span>
    
- <span data-ttu-id="bb778-117">modifiez la distance indiquée dans la cellule PageScale du même facteur que la cellule DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="bb778-117">Change the distance expressed in the PageScale cell by the same factor that you change DrawingScale.</span></span>
    
<span data-ttu-id="bb778-118">Pour obtenir une référence à la cellule DrawingScale par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="bb778-118">To get a reference to the DrawingScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb778-119">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="bb778-119">Cell name:</span></span>  <br/> |<span data-ttu-id="bb778-120">DrawingScale</span><span class="sxs-lookup"><span data-stu-id="bb778-120">DrawingScale</span></span>  <br/> |
   
<span data-ttu-id="bb778-121">Pour obtenir une référence à la cellule DrawingScale à l'aide d'un index à partir d'un programme
, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bb778-121">To get a reference to the DrawingScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb778-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bb778-122">Section index:</span></span>  <br/> |<span data-ttu-id="bb778-123">**Définis**</span><span class="sxs-lookup"><span data-stu-id="bb778-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bb778-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bb778-124">Row index:</span></span>  <br/> |<span data-ttu-id="bb778-125">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="bb778-125">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="bb778-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bb778-126">Cell index:</span></span>  <br/> |<span data-ttu-id="bb778-127">**visPageDrawingScale**</span><span class="sxs-lookup"><span data-stu-id="bb778-127">**visPageDrawingScale**</span></span> <br/> |
   

