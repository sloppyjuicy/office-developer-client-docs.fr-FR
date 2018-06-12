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
ms.openlocfilehash: 7724466b6ad225fcf39243bc80ba2e440f3b700b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788333"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a>ConLineRouteExt, cellule (section Shape Layout)

Détermine l'aspect d'un connecteur.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Valeur par défaut ; utilise le paramètre de la page  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Droit  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Courbé  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule ConLineTouteExt par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ConLineRouteExt  <br/> |
   
Pour obtenir une référence à la cellule ConLineRouteExt par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
| Index de la cellule :  <br/> |**visSLOLineRouteExt** <br/> |
   

