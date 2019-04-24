---
title: TxtHeight, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Détermine la hauteur du bloc de texte. La formule par défaut est la suivante :'
ms.openlocfilehash: 8ad17cdf1deca6c4aa81f3388d7c112b4e179e2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334390"
---
# <a name="txtheight-cell-text-transform-section"></a>TxtHeight, cellule (section Text Transform)

Détermine la hauteur du bloc de texte. La formule par défaut est la suivante :
  
= Hauteur \* 1
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtHeight par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TxtHeight  <br/> |
   
Pour obtenir une référence à la cellule TxtHeight par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowTextXForm** <br/> |
| Index de la cellule :  <br/> |**visXFormHeight** <br/> |
   

