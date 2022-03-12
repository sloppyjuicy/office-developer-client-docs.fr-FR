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
ms.openlocfilehash: 0365418825e515a3d521825e5606c99fdb7e7644
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448537"
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

Vous pouvez déterminer le système de mesure d'un dessin en examinant la propriété **Units** de la cellule DrawingScale. Après avoir exécuté la macro ci-dessus, la déclaration suivante exécutée dans la fenêtre Exécution de Visual Basic Editor renvoie de nouveau la valeur *True*.
  
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
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |DrawingScale  <br/> |

Pour obtenir une référence à la cellule DrawingScale à l'aide d'un index à partir d'un programme
, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPage** <br/> |
|**Index de la cellule :**  <br/> |**visPageDrawingScale** <br/> |
