---
title: Width, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: "Contient la largeur de la forme sélectionnée, exprimée en unités de dessin. La formule par défaut permettant de déterminer la largeur d'une forme 1D est la suivante :"
ms.openlocfilehash: c99f4669f3b27390a5b8e9062d6085a5a9db54e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415193"
---
# <a name="width-cell-shape-transform-section"></a>Width, cellule (section Shape Transform)

Contient la largeur de la forme sélectionnée, exprimée en unités de dessin. La formule par défaut permettant de déterminer la largeur d'une forme 1D est la suivante :
  
= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Width par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Largeur  <br/> |
   
Pour obtenir une référence à la cellule Width par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormWidth** <br/> |
   

