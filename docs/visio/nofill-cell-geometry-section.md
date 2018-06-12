---
title: NoFill, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Indique si un chemin peut être rempli.
ms.openlocfilehash: 3f5bab76fc38b6e82aeaeee45b75bd733afdbd26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789169"
---
# <a name="nofill-cell-geometry-section"></a>NoFill, cellule (section Geometry)

Indique si un chemin peut être rempli.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le chemin n'est pas rempli, même si d'autres chemins de la forme sont remplis.  <br/> |
| FALSE  <br/> | Le remplissage de la forme s'applique au chemin, même s'il n'est pas fermé.  <br/> |
   
## <a name="remarks"></a>Note

Si vous définissez le motif de remplissage de la forme sur aucun (0), aucun de ses chemins ne sera rempli. Cette cellule est utilisée pour désactiver de manière sélective le remplissage du chemin d'une forme.
  
Pour obtenir une référence à la cellule NoFill par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Géométrie *i* . NoFill où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule NoFill par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionFirstComponent** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la ligne :  <br/> |**visRowComponent** <br/> |
| Index de la cellule :  <br/> |**visCompNoFill** <br/> |
   

