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
ms.openlocfilehash: ffb32cf8c0506eb8b4064f455258a7153bc123df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623319"
---
# <a name="nosnap-cell-geometry-section"></a>NoSnap, cellule (section Geometry)

Détermine si les autres formes s'alignent sur un chemin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Ne permet pas aux autres formes de s'aligner sur ce chemin.  <br/> |
| FALSE  <br/> | Permet aux autres formes de s'aligner sur ce chemin.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NoSnap par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Geometry  *i*  . NoSnap où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule NoSnap à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowComponent** <br/> |
| Index de la cellule :  <br/> |**visCompNoSnap** <br/> |
   

