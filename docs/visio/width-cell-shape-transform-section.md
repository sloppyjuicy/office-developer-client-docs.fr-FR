---
title: Width, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
ms.localizationpriority: medium
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: "Contient la largeur de la forme sélectionnée, exprimée en unités de dessin. La formule par défaut permettant de déterminer la largeur d'une forme 1D est la suivante :"
ms.openlocfilehash: 90973f93d3c5ebb04362775cedc3c6753471f8c7
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634288"
---
# <a name="width-cell-shape-transform-section"></a>Width, cellule (section Shape Transform)

Contient la largeur de la forme sélectionnée, exprimée en unités de dessin. La formule par défaut permettant de déterminer la largeur d'une forme 1D est la suivante :
  
= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Width par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | Largeur  <br/> |
   
Pour obtenir une référence à la cellule Width par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowXFormOut** <br/> |
| **Index de la cellule :**  <br/> |**visXFormWidth** <br/> |
   

