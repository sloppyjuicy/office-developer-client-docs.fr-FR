---
title: LockRotate, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Empêche les formes 2D en rotation avec la poignée de rotation ou la faire pivoter à gauche de 90° ou commande de 90° faire pivoter à droite.
ms.openlocfilehash: 450fe4786594472d018b705df4678fe636390ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789015"
---
# <a name="lockrotate-cell-protection-section"></a>LockRotate, cellule (section Protection)

Verrouille avec la poignée de rotation ou la **faire pivoter à gauche de 90 °** ou **faire pivoter à droite de 90 °** commande pivoter les formes 2D. 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La rotation de la forme est impossible.  <br/> |
| FALSE  <br/> | La rotation de la forme est possible (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Note

La cellule LockRotate n'empêche pas de faire pivoter une forme 1D lorsque vous faites glisser une extrémité. Pour verrouiller une forme 1D afin d'empêcher sa rotation, attribuez une valeur différente de zéro à la cellule LockWidth (TRUE).
  
Pour obtenir une référence à la cellule LockRotate par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LockRotate  <br/> |
   
Pour obtenir une référence à la cellule LockRotate par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLock** <br/> |
| Index de la cellule :  <br/> |**visLockRotate** <br/> |
   

