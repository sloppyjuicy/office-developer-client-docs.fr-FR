---
title: Y, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
ms.localizationpriority: medium
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Représente la coordonnée y d’un point de connexion dans les coordonnées locales.
ms.openlocfilehash: 6b840b66e41a44322f831d49ef4ea54c3954c95c
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626835"
---
# <a name="y-cell-connection-points-section"></a>Y, cellule (section Connection Points)

Représente la coordonnée  *y*  d’un point de connexion dans les coordonnées locales. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Connections.Y  *i*            où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionConnectionPts** <br/> |
| **Index de la ligne :**  <br/> |**visRowConnectionPts** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visY** <br/> |
   

