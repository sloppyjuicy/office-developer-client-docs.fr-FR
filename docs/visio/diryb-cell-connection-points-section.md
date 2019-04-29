---
title: DirY / B, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Détermine le composant y pour le vecteur d'alignement requis d'un point de connexion correspondant. Cette cellule sert également à orienter la branche reliée d'un lien dynamique. Elle accepte une valeur à virgule flottante.
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417090"
---
# <a name="diry--b-cell-connection-points-section"></a>DirY / B, cellule (section Connection Points)

Détermine le composant *y* pour le vecteur d'alignement requis d'un point de connexion correspondant. Cette cellule sert également à orienter la branche reliée d'un lien dynamique. Cette cellule prend pour valeur un réel à virgule flottante. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule DirY / B par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Connections. DirY [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule DirY / B à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionConnectionPts** <br/> |
|Index de la ligne :  <br/> |**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCnnctDirY** (lignes non étendues)           **visCnnctB** (lignes étendues)  <br/> |
   
Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.
  

