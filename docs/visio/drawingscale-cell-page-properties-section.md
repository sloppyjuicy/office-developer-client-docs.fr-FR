---
title: DrawingScale, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm265
ms.localizationpriority: medium
ms.assetid: bc447f22-a188-2c61-e33c-df0d401a4725
description: Représente la valeur de l'unité de dessin dans l'échelle de dessin en cours. L'échelle de dessin est le rapport entre l'unité de page représentée dans la cellule PageScale et l'unité de dessin représentée dans la cellule DrawingScale.
ms.openlocfilehash: f1e0ff314aea587334550568ae5067e3acdceec4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586536"
---
# <a name="drawingscale-cell-page-properties-section"></a>DrawingScale, cellule (section Page Properties)

Représente la valeur de l'unité de dessin dans l'échelle de dessin en cours. L'échelle de dessin est le rapport entre l'unité de page représentée dans la cellule PageScale et l'unité de dessin représentée dans la cellule DrawingScale.
  
Vous pouvez définir la cellule DrawingScale de manière à modifier les unités de la règle à partir d'un programme. Voici un exemple qui montre comment changer en centimètres les unités exprimées en pouces à partir d'un programme. Ici, nous utilisons la méthode **ConvertResult** pour conserver la même distance et l'exprimer dans une unité différente. 
  
```vb
Public Sub SetActivePageMeasurementToCM() 
Dim dsCell As Visio.Cell 
Set dsCell = ActivePage.PageSheet.Cells("DrawingScale") 
 dsCell.Result(visCentimeters) = _ 
 Application.ConvertResult _ 
 (dsCell.ResultIU,visInches,visCentimeters) 
End Sub 
```

Vous pouvez déterminer le système de mesure d'un dessin en examinant la propriété **Units** de la cellule DrawingScale. Après avoir exécuté la macro ci-dessus, l’instruction suivante exécutée dans la Visual Basic Exécution de l’éditeur retourne *la valeur True* . 
  
```vb
debug.print ActivePage.PageSheet.Cells("DrawingScale").Units = _ 
 visCentimeters 
```

## <a name="remarks"></a>Remarques

Cette cellule correspond aux paramètres de la boîte de dialogue **Mise en page** (cliquez sur la flèche **Mise en page** sous l’onglet **Accueil**). 
  
Les unités de la formule contenue dans la cellule DrawingScale définissent également les unités de mesure des règles dans la fenêtre de dessin. Si vous ne souhaitez pas modifier en même temps l'échelle du dessin, vous pouvez procéder de l'une des manières suivantes :
  
- conservez la distance indiquée dans la cellule DrawingScale, mais convertissez-la dans une unité différente ;
    
- modifiez la distance indiquée dans la cellule PageScale du même facteur que la cellule DrawingScale.
    
Pour obtenir une référence à la cellule DrawingScale par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |DrawingScale  <br/> |
   
Pour obtenir une référence à la cellule DrawingScale à l'aide d'un index à partir d'un programme
, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPage** <br/> |
|Index de la cellule :  <br/> |**visPageDrawingScale** <br/> |
   

