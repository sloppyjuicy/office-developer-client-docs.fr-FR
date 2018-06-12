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
description: Cellule event qui est évaluée lorsque la position ou l’orientation de la page d’une forme est transformé (XF).
ms.openlocfilehash: 5884aabc11798ae0440fbfa024b9cc2f2418b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788596"
---
# <a name="eventxfmod-cell-events-section"></a>EventXFMod, cellule (section Events)

Cellule Event qui est évaluée lorsque la position ou l'orientation d'une forme sur la page est modifiée (« XF »).
  
## <a name="remarks"></a>Note

Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.
  
Pour obtenir une référence à la cellule EventXFMod par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | EventXFMod  <br/> |
   
Pour obtenir une référence à la cellule EventXFMod par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowEvent** <br/> |
| Index de la cellule :  <br/> |**visEvtCellXFMod** <br/> |
   

