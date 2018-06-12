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
ms.openlocfilehash: ecba66aaf1f7eeb6d16c6b0d4c6569aed051910f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789969"
---
# <a name="txtwidth-cell-text-transform-section"></a>TxtWidth, cellule (section Text Transform)

Détermine la largeur du bloc de texte. La formule par défaut est la suivante :
  
= Largeur \* 1
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule TxtWidth par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TxtWidth  <br/> |
   
Pour obtenir une référence à la cellule TxtWidth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowTextXForm** <br/> |
| Index de la cellule :  <br/> |**visXFormWidth** <br/> |
   

