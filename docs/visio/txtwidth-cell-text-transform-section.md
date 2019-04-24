---
title: TxtWidth, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Détermine la largeur du bloc de texte. La formule par défaut est la suivante :'
ms.openlocfilehash: 806307166035ebc2f8e20e7025d5ecb03c4d6e79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316001"
---
# <a name="txtwidth-cell-text-transform-section"></a>TxtWidth, cellule (section Text Transform)

Détermine la largeur du bloc de texte. La formule par défaut est la suivante :
  
= Largeur \* 1
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule TxtWidth par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TxtWidth  <br/> |
   
Pour obtenir une référence à la cellule TxtWidth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowTextXForm** <br/> |
| Index de la cellule :  <br/> |**visXFormWidth** <br/> |
   

