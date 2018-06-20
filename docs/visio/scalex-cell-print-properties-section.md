---
title: ScaleX, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Indique le pourcentage d’agrandissement de la page de dessin sur la page d’impression.
ms.openlocfilehash: 1713e88f06dc93a2806e64cae3d7af20c9df1fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789597"
---
# <a name="scalex-cell-print-properties-section"></a>ScaleX, cellule (section Print Properties)

Indique le pourcentage d’agrandissement de la page de dessin sur la page d’impression.
  
## <a name="remarks"></a>Remarques

Cette valeur est utilisée uniquement lorsque la valeur de la cellule OnPage est FALSE. Les cellules ScaleX et ScaleY ont toujours la même valeur, qui correspond à la valeur du paramètre **Ajuster sur** sous l’onglet **Configuration de l’impression** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ). 
  
Pour obtenir une référence à la cellule ScaleX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |ScaleX  <br/> |
   
Pour obtenir une référence à la cellule ScaleX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
|Index de la cellule :  <br/> |**visPrintPropertiesScaleX** <br/> |
   

