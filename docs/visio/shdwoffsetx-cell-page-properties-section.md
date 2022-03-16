---
title: ShdwOffsetX, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
ms.localizationpriority: medium
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Détermine, en unités de page, la distance du décalage horizontal entre l'ombre d'une forme et la forme.
ms.openlocfilehash: 8fdd860201473a3bc046b078acf82b87247e3379
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63508241"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a>ShdwOffsetX, cellule (section Page Properties)

Détermine, en unités de page, la distance du décalage horizontal entre l'ombre d'une forme et la forme.
  
## <a name="remarks"></a>Remarques

Cette valeur est définie dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**). Elle est indépendante de l’échelle du dessin. Si le dessin est mis à l’échelle, le décalage de l’ombre reste le même. 
  
Pour obtenir une référence à la cellule ShdwOffsetX par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | ShdwOffsetX  <br/> |
   
Pour obtenir une référence à la cellule ShdwOffsetX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPage** <br/> |
| **Index de la cellule :**  <br/> |**visPageShdwOffsetX** <br/> |
   

