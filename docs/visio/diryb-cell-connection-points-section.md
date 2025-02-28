---
title: DirY / B, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
ms.localizationpriority: medium
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Détermine le composant y pour le vecteur d’alignement requis d’un point de connexion correspondant. Cette cellule sert également à orienter la branche reliée d'un lien dynamique. Elle accepte une valeur à virgule flottante.
ms.openlocfilehash: 34b0511b6a3aac181f932696f08c95123b814e65
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406231"
---
# <a name="diry--b-cell-connection-points-section"></a>DirY / B, cellule (section Connection Points)

Détermine le *composant y* pour le vecteur d’alignement requis d’un point de connexion correspondant. Cette cellule sert également à orienter la branche reliée d'un lien dynamique. Cette cellule prend pour valeur un réel à virgule flottante.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule DirY / B par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Connections.DirY[*i*]           <br/>où *i* = <1>, 2, 3... |

Pour obtenir une référence à la cellule DirY / B à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionConnectionPts** <br/> |
|**Index de la ligne :**  <br/> |**visRowConnectionPts** +  *i*           <br/>où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visCnnctDirY** (lignes non étendues)          <br/>**visCnnctB** (lignes étendues)  <br/> |

Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.
  