---
title: ScaleX, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
ms.localizationpriority: medium
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Spécifie le pourcentage d’agrandissement de la page de dessin sur la page d’impression.
ms.openlocfilehash: 44dd72b6605b400c5ed93e76fe32e44bc45f47c2
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521392"
---
# <a name="scalex-cell-print-properties-section"></a>ScaleX, cellule (section Print Properties)

Spécifie le pourcentage d’agrandissement de la page de dessin sur la page d’impression.
  
## <a name="remarks"></a>Remarques

Cette valeur n’est utilisée que lorsque la valeur de la cellule OnPage est FALSE. Les cellules ScaleX et ScaleY ont toujours la même valeur, ce qui correspond à la valeur du paramètre  Ajuster à sous l’onglet Configuration de l’impression de la boîte de dialogue Mise  en **page** (sous l’onglet Création, cliquez sur la flèche Mise en **page**). 
  
Pour obtenir une référence à la cellule ScaleX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |ScaleX  <br/> |
   
Pour obtenir une référence à la cellule ScaleX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPrintProperties** <br/> |
|**Index de la cellule :**  <br/> |**visPrintPropertiesScaleX** <br/> |
   

