---
title: EventXFMod, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: Cellule Event qui est évaluée lorsque la position ou l'orientation d'une forme sur la page est modifiée (XF).
ms.openlocfilehash: c4ed4ddd9b255a9a52fc81349b514dbd25772c98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418532"
---
# <a name="eventxfmod-cell-events-section"></a>EventXFMod, cellule (section Events)

Cellule Event qui est évaluée lorsque la position ou l'orientation d'une forme sur la page est modifiée (« XF »).
  
## <a name="remarks"></a>Remarques

Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.
  
Pour obtenir une référence à la cellule EventXFMod par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | EventXFMod  <br/> |
   
Pour obtenir une référence à la cellule Event XFMod à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowEvent** <br/> |
| Index de la cellule :  <br/> |**visEvtCellXFMod** <br/> |
   

