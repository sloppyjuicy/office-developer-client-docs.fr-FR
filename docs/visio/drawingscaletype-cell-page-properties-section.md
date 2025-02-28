---
title: DrawingScaleType, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
ms.localizationpriority: medium
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Détermine l’échelle de dessin sélectionnée dans la boîte de dialogue Mise en page (cliquez sur la flèche Mise en page sous l’onglet Accueil).
ms.openlocfilehash: 647df1d62efa71d32af432d847ccaab025f7facc
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522162"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>DrawingScaleType, cellule (section Page Properties)

Détermine l’échelle de dessin sélectionnée dans la boîte de dialogue **Mise en page** (cliquez sur la flèche **Mise en page** sous l’onglet **Accueil**). 
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Pas d'échelle  <br/> |**visNoScale** <br/> |
| 1  <br/> | Échelle architecturale  <br/> |**visArchitectural** <br/> |
| 2  <br/> | Échelle Génie civil  <br/> |**visEngineering** <br/> |
| 3  <br/> | Échelle personnalisée  <br/> |**visScaleCustom** <br/> |
| 4  <br/> | Métrique  <br/> |**visScaleMetric** <br/> |
| 5  <br/> | Échelle Génie mécanique  <br/> |**visScaleMechanical** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule DrawingScaleType par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | DrawingScaleType  <br/> |
   
Pour obtenir une référence à la cellule DrawingScaleType à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPage** <br/> |
| **Index de la cellule :**  <br/> |**visPageDrawScaleType** <br/> |
   

