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
ms.openlocfilehash: e9495eef837a61fa9b7ecb2b242fdabc5df30080
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789949"
---
# <a name="txtheight-cell-text-transform-section"></a>TxtHeight, cellule (section Text Transform)

Détermine la hauteur du bloc de texte. La formule par défaut est la suivante :
  
= Hauteur \* 1
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule TxtHeight par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TxtHeight  <br/> |
   
Pour obtenir une référence à la cellule TxtHeight par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowTextXForm** <br/> |
| Index de la cellule :  <br/> |**visXFormHeight** <br/> |
   

