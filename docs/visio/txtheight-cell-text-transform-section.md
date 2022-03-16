---
title: TxtHeight, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
ms.localizationpriority: medium
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Détermine la hauteur du bloc de texte. La formule par défaut est la suivante :'
ms.openlocfilehash: 29f5c2c855258a7b490c29913b57b26f794c5bc2
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507442"
---
# <a name="txtheight-cell-text-transform-section"></a>TxtHeight, cellule (section Text Transform)

Détermine la hauteur du bloc de texte. La formule par défaut est la suivante :
  
= Hauteur \* 1
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtHeight par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | TxtHeight  <br/> |
   
Pour obtenir une référence à la cellule TxtHeight par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowTextXForm** <br/> |
| **Index de la cellule :**  <br/> |**visXFormHeight** <br/> |
   

