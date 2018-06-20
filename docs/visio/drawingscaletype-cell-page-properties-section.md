---
title: DrawingScaleType, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Détermine l’échelle de dessin sélectionnée dans la boîte de dialogue Mise en Page (cliquez sur la flèche mise en Page sous l’onglet Accueil).
ms.openlocfilehash: b93bd95a30fe5a8a5de15a8e5ea104279cf1bcda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788531"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>DrawingScaleType, cellule (section Page Properties)

Détermine l’échelle de dessin sélectionnée dans la boîte de dialogue **Mise en Page** (cliquez sur la flèche **Mise en Page** sous l’onglet **accueil** ). 
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Pas d'échelle  <br/> |**visNoScale** <br/> |
| 1  <br/> | Échelle architecturale  <br/> |**visArchitectural** <br/> |
| 2  <br/> | Échelle Génie civil  <br/> |**visEngineering** <br/> |
| 3  <br/> | Échelle personnalisée  <br/> |**visScaleCustom** <br/> |
| 4  <br/> | Métrique  <br/> |**visScaleMetric** <br/> |
| 5  <br/> | Échelle Génie mécanique  <br/> |**visScaleMechanical** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule DrawingScaleType par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | DrawingScaleType  <br/> |
   
Pour obtenir une référence à la cellule DrawingScaleType par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageDrawScaleType** <br/> |
   

