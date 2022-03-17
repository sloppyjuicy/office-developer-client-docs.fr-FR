---
title: NoShow, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
ms.localizationpriority: medium
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Indique si un chemin est affiché sur la page de dessin.
ms.openlocfilehash: a18e7d556b25fe21f72808e77061a37bece65386
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63519705"
---
# <a name="noshow-cell-geometry-section"></a>NoShow, cellule (section Geometry)

Indique si un chemin est affiché sur la page de dessin.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le trait et le remplissage du chemin représentés par cette section sont masqués. |
| FALSE  <br/> | Le trait et le remplissage du chemin sont affichés. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NoShow par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Geometry  *i*  . NoShow où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule NoShow à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionFirstComponent** +   *i* où *i* = 0, 1, 2... |
| **Index de la ligne :**  <br/> |**visRowComponent** <br/> |
| **Index de la cellule :**  <br/> |**visCompNoShow** <br/> |
   

