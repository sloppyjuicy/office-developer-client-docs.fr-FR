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
ms.openlocfilehash: cdd3222f5e56c34ac8947c9ef5a653cfe19fbd0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788510"
---
# <a name="drawingscale-cell-page-properties-section"></a><span data-ttu-id="58812-104">DrawingScale, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="58812-104">DrawingScale Cell (Page Properties Section)</span></span>

<span data-ttu-id="58812-p102">Représente la valeur de l'unité de dessin dans l'échelle de dessin en cours. L'échelle de dessin est le rapport entre l'unité de page représentée dans la cellule PageScale et l'unité de dessin représentée dans la cellule DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="58812-p102">Represents the value of the drawing unit in the current drawing scale. The drawing scale for the page is the ratio of the page unit shown in the PageScale cell to the drawing unit shown in the DrawingScale cell.</span></span>
  
<span data-ttu-id="58812-107">Vous pouvez définir la cellule DrawingScale pour modifier les unités des règles d’une page à partir d’un programme.</span><span class="sxs-lookup"><span data-stu-id="58812-107">You can set the DrawingScale cell to change the units of a page's rulers from a program.</span></span> <span data-ttu-id="58812-108">Voici un exemple de modification de l’unité de mesure en pouces en centimètres à partir d’un programme.</span><span class="sxs-lookup"><span data-stu-id="58812-108">Here is an example of changing the measurement units from inches to centimeters from a program.</span></span> <span data-ttu-id="58812-109">Dans ce cas, nous utilisons la méthode **ConvertResult** pour conserver la distance mais convertissez-la dans une unité différente.</span><span class="sxs-lookup"><span data-stu-id="58812-109">In this case, we use the **ConvertResult** method to keep the distance the same but express it in different units.</span></span> 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

<span data-ttu-id="58812-110">Vous pouvez déterminer le système de mesure dans un dessin en examinant la propriété **Units** de la cellule DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="58812-110">You can determine the measurement system in a drawing by examining the **Units** property of the DrawingScale cell.</span></span> <span data-ttu-id="58812-111">Après avoir exécuté la macro ci-dessus, la déclaration suivante exécutée dans l’exécution de Visual Basic Editor fenêtre renvoie *la valeur True* .</span><span class="sxs-lookup"><span data-stu-id="58812-111">After running the above macro the following statement executed in the Visual Basic Editor Immediate window will return  *True*  .</span></span> 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a><span data-ttu-id="58812-112">Note</span><span class="sxs-lookup"><span data-stu-id="58812-112">Remarks</span></span>

<span data-ttu-id="58812-113">Cette cellule correspond aux paramètres de la boîte de dialogue **Mise en Page** (cliquez sur la flèche **Mise en Page** sous l’onglet **accueil** ).</span><span class="sxs-lookup"><span data-stu-id="58812-113">This cell corresponds to the settings in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="58812-p105">Les unités de la formule contenue dans la cellule DrawingScale définissent également les unités de mesure des règles dans la fenêtre de dessin. Si vous ne souhaitez pas modifier en même temps l'échelle du dessin, vous pouvez procéder de l'une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="58812-p105">The units of the formula in the DrawingScale cell determine the measurement units used by the rulers in the drawing window. If you do not want to also change the drawing's scale, you can do one of the following:</span></span>
  
- <span data-ttu-id="58812-116">conservez la distance indiquée dans la cellule DrawingScale, mais convertissez-la dans une unité différente ;</span><span class="sxs-lookup"><span data-stu-id="58812-116">Keep the distance expressed in the DrawingScale cell the same but express it in different units.</span></span>
    
- <span data-ttu-id="58812-117">modifiez la distance indiquée dans la cellule PageScale du même facteur que la cellule DrawingScale.</span><span class="sxs-lookup"><span data-stu-id="58812-117">Change the distance expressed in the PageScale cell by the same factor that you change DrawingScale.</span></span>
    
<span data-ttu-id="58812-118">Pour obtenir une référence à la cellule DrawingScale par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="58812-118">To get a reference to the DrawingScale cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58812-119">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="58812-119">Cell name:</span></span>  <br/> |<span data-ttu-id="58812-120">DrawingScale</span><span class="sxs-lookup"><span data-stu-id="58812-120">DrawingScale</span></span>  <br/> |
   
<span data-ttu-id="58812-121">Pour obtenir une référence à la cellule DrawingScale par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="58812-121">To get a reference to the DrawingScale cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58812-122">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="58812-122">Section index:</span></span>  <br/> |<span data-ttu-id="58812-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="58812-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="58812-124">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="58812-124">Row index:</span></span>  <br/> |<span data-ttu-id="58812-125">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="58812-125">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="58812-126">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="58812-126">Cell index:</span></span>  <br/> |<span data-ttu-id="58812-127">**visPageDrawingScale**</span><span class="sxs-lookup"><span data-stu-id="58812-127">**visPageDrawingScale**</span></span> <br/> |
   

