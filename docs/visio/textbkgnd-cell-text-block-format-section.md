---
title: TextBkgnd, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
ms.localizationpriority: medium
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Détermine la couleur d'arrière-plan du texte dans une forme.
ms.openlocfilehash: b6390e03f143d748757aec1aad48341579310c69
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506043"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>TextBkgnd, cellule (section Text Block Format)

Détermine la couleur d'arrière-plan du texte dans une forme.
  
## <a name="remarks"></a>Remarques

La cellule TextBkgnd peut avoir une valeur comprise entre 0 et 24, ou 255. Les valeurs 0 et 255 ( *visTxtBlklOpaque*) indiquent toutes deux un arrière-plan de texte transparent. 
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL plus un : par exemple RVB(255,127,255) +1. La valeur d’une couleur personnalisée est sa couleur RVB, et RVB( *r, g, b*)+1, au lieu d’un nombre, s’affiche dans la fenêtre Feuille ShapeSheet. Lorsqu'elles sont utilisées dans les opérations numériques, les couleurs personnalisées ont des valeurs de 25 et supérieures. 
  
Vous pouvez définir la transparence de la couleur du texte d'arrière-plan dans la cellule TextBkgndTrans.
  
Pour obtenir une référence à la cellule TextBkgnd par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |TextBkgnd  <br/> |
   
Pour obtenir une référence à la cellule TextBkgnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowText** <br/> |
|**Index de la cellule :**  <br/> |**visTxtBlkBkgnd** <br/> |
   

