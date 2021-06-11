---
title: ConLineRouteExt, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Détermine l'aspect d'un connecteur.
ms.openlocfilehash: 19fe948daf7aa3d67db858849ecb2b15f40ba02d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434612"
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
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ConLineRouteExt  <br/> |
   
Pour obtenir une référence à la cellule ConLineRouteExt à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
| Index de la cellule :  <br/> |**visSLOLineRouteExt** <br/> |
   

