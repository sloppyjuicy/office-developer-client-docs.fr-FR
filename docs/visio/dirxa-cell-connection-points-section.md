---
title: DirX / A, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
ms.localizationpriority: medium
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Détermine le composant x pour le vecteur d’alignement requis d’un point de connexion correspondant. La cellule DirX / A sert également à orienter la branche reliée d'un connecteur dynamique. Cette cellule prend pour valeur un réel à virgule flottante.
ms.openlocfilehash: 518bacb7a5ccd1747998c38ff9545f09e916f486
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63447654"
---
# <a name="dirx--a-cell-connection-points-section"></a>DirX / A, cellule (section Connection Points)

Détermine le  *composant x pour*  le vecteur d’alignement requis d’un point de connexion correspondant. La cellule DirX / A sert également à orienter la branche reliée d'un connecteur dynamique. Cette cellule prend pour valeur un réel à virgule flottante. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule DirX / A par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Connections.DirX[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule DirX / A à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionConnectionPts** <br/> |
| **Index de la ligne :**  <br/> |**visRowConnectionPts** +   *i* où *i* = 0, 1, 2  <br/> |
| **Index de la cellule :**  <br/> |**visCnnctDirX** (lignes non étendues)           **visCnnctA** (lignes étendues)  <br/> |
   
Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.
  

