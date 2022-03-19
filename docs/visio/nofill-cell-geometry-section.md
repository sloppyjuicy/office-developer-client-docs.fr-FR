---
title: NoFill, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
ms.localizationpriority: medium
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Indique si un chemin peut être rempli.
ms.openlocfilehash: 3206666f406cac9eb665732d3c34c5758fc0ae49
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634778"
---
# <a name="nofill-cell-geometry-section"></a>NoFill, cellule (section Geometry)

Indique si un chemin peut être rempli.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le chemin n'est pas rempli, même si d'autres chemins de la forme sont remplis. |
| FALSE  <br/> | Le remplissage de la forme s'applique au chemin, même s'il n'est pas fermé. |
   
## <a name="remarks"></a>Remarques

Si vous définissez le motif de remplissage de la forme sur aucun (0), aucun de ses chemins ne sera rempli. Cette cellule est utilisée pour désactiver de manière sélective le remplissage du chemin d'une forme.
  
Pour obtenir une référence à la cellule NoFill par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Geometry  *i*  . NoFill où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule NoFill à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionFirstComponent** +   *i* où *i* = 0, 1, 2... |
| **Index de la ligne :**  <br/> |**visRowComponent** <br/> |
| **Index de la cellule :**  <br/> |**visCompNoFill** <br/> |
   

