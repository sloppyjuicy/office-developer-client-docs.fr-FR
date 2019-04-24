---
title: ScaleY, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Indique le pourcentage d'agrandissement de la page de dessin sur la page de l'imprimante.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342727"
---
# <a name="scaley-cell-print-properties-section"></a>ScaleY, cellule (section Print Properties)

Indique le pourcentage d'agrandissement de la page de dessin sur la page de l'imprimante.
  
## <a name="remarks"></a>Remarques

Cette valeur n’est utilisée que lorsque la valeur de la cellule OnPage est FALSE. Les cellules ScaleX et ScaleY ont toujours la même valeur, ce qui correspond à la valeur du paramètre ajuster sur dans l'onglet **configuration** de l'impression de la boîte de dialogue **mise en page** (sous l'onglet **création** , cliquez sur la flèche mise **en** **page** ). 
  
Pour obtenir une référence à la cellule ScaleY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ScaleY  <br/> |
   
Pour obtenir une référence à la cellule ScaleY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
|Index de la cellule :  <br/> |**visPrintPropertiesScaleY** <br/> |
   

