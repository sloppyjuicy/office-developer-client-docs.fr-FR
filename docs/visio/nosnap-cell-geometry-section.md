---
title: NoSnap, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Détermine si les autres formes s'alignent sur un chemin.
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408543"
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
| Nom de la cellule :  <br/> | Géométrie *i* . NoSnap où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule NoSnap à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowComponent** <br/> |
| Index de la cellule :  <br/> |**visCompNoSnap** <br/> |
   

