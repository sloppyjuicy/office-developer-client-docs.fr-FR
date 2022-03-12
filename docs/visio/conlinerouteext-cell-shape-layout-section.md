---
title: ConLineRouteExt, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
ms.localizationpriority: medium
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Détermine l'aspect d'un connecteur.
ms.openlocfilehash: 55f71d77892a1036879c1db8c5a5431199536dd5
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448712"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a>ConLineRouteExt, cellule (section Shape Layout)

Détermine l'aspect d'un connecteur.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Valeur par défaut ; utilise le paramètre de la page  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Droite  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Courbe  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule ConLineTouteExt par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | ConLineRouteExt  <br/> |
   
Pour obtenir une référence à la cellule ConLineRouteExt à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowShapeLayout** <br/> |
| **Index de la cellule :**  <br/> |**visSLOLineRouteExt** <br/> |
   

