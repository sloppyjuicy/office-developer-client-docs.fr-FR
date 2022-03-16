---
title: X, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
ms.localizationpriority: medium
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Représente la coordonnée x d’un point de connexion en coordonnées locales.
ms.openlocfilehash: 82fb8c17be9ccbddb8f14356cf1fcb30bd2e18f0
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507667"
---
# <a name="x-cell-connection-points-section"></a>X, cellule (section Connection Points)

Représente la  *coordonnée x d’un*  point de connexion en coordonnées locales. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Connections.X  *i*            où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionConnectionPts** <br/> |
| **Index de la ligne :**  <br/> |**visRowConnectionPts** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visX** <br/> |
   

