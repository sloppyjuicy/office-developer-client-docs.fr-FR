---
title: NoSnap, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
ms.localizationpriority: medium
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Détermine si les autres formes s'alignent sur un chemin.
ms.openlocfilehash: 425ebee1d0a96a16210520a1f56045bb4fdcabd9
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631728"
---
# <a name="nosnap-cell-geometry-section"></a>NoSnap, cellule (section Geometry)

Détermine si les autres formes s'alignent sur un chemin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Ne permet pas aux autres formes de s'aligner sur ce chemin. |
| FALSE  <br/> | Permet aux autres formes de s'aligner sur ce chemin. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NoSnap par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Geometry  *i*  . NoSnap où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule NoSnap à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionFirstComponent** +   *i* où *i* = 0, 1, 2... |
| **Index de la ligne :**  <br/> |**visRowComponent** <br/> |
| **Index de la cellule :**  <br/> |**visCompNoSnap** <br/> |
   

