---
title: LockRotate, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
ms.localizationpriority: medium
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Empêche de faire pivoter les formes 2D avec la poignée de rotation ou la commande Faire pivoter à gauche de 90° ou Faire pivoter à droite de 90°.
ms.openlocfilehash: ef55d75309af509f73bff8d422e0f6406715df95
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520321"
---
# <a name="lockrotate-cell-protection-section"></a>LockRotate, cellule (section Protection)

Empêche de faire pivoter les formes 2D avec la poignée de rotation ou la commande **Faire pivoter à gauche de 90°** ou **Faire pivoter à droite de 90°**. 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La rotation de la forme est impossible. |
| FALSE  <br/> | La rotation de la forme est possible (valeur par défaut). |
   
## <a name="remarks"></a>Remarques

La cellule LockRotate n'empêche pas de faire pivoter une forme 1D lorsque vous faites glisser une extrémité. Pour verrouiller une forme 1D afin d'empêcher sa rotation, attribuez une valeur différente de zéro à la cellule LockWidth (TRUE).
  
Pour obtenir une référence à la cellule LockRotate par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | LockRotate  <br/> |
   
Pour obtenir une référence à la cellule LockRotate à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowLock** <br/> |
| **Index de la cellule :**  <br/> |**visLockRotate** <br/> |
   

