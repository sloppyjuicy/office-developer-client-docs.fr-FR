---
title: Y Behavior, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1190
ms.localizationpriority: medium
ms.assetid: 6d5062d3-743b-8664-8ec9-5a8f11d5edf9
description: Contrôle le type de comportement de la coordonnée y de la poignée de contrôle une fois le handle déplacé. Les formules suivantes sont disponibles.
ms.openlocfilehash: e86b96cf4fad0959b42ae458d61b233d728825cd
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63523093"
---
# <a name="y-behavior-cell-controls-section"></a>Y Behavior, cellule (section Controls)

Contrôle le type de comportement de la coordonnée  *y*  de la poignée de contrôle une fois le handle déplacé. Les formules suivantes sont disponibles. 
  
|**Valeur**|**Comportement**|**Définition**|**Constante d'automation**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | Proportionnel  <br/> | La poignée de contrôle peut être déplacée et se déplace proportionnellement à la forme lorsque cette dernière est redimensionnée. |**visCtlProportional** <br/> |
| 1  <br/> | Proportionnel verrouillé  <br/> | La poignée de contrôle se déplace proportionnellement à la forme lorsque cette dernière est redimensionnée mais ne peut être déplacée indépendamment de la forme. |**visCtlLocked** <br/> |
| 2  <br/> | Décalé du bord inférieur  <br/> | La poignée de contrôle est décalée d'une valeur constante par rapport au bas de la forme. |**visCtlOffsetMin** <br/> |
| 3  <br/> | Décalé du centre  <br/> | La poignée de contrôle est décalée d'une valeur constante par rapport au centre de la forme. |**visCtlOffsetMid** <br/> |
| 4  <br/> | Décalé du bord supérieur  <br/> | La poignée de contrôle est décalée d'une valeur constante par rapport au haut de la forme. |**visCtlOffsetMax** <br/> |
| 5  <br/> | Proportionnel, masqué  <br/> | Identique à 0 mais la poignée de contrôle n'est pas visible. |**visCtlProportionalHidden** <br/> |
| 6   <br/> | Proportionnel verrouillé, masqué  <br/> | Identique à 1 mais la poignée de contrôle n'est pas visible. |**visCtlLockedHiddenv** <br/> |
| 7   <br/> | Décalé du bord gauche, masqué  <br/> | Identique à 2 mais la poignée de contrôle n'est pas visible. |**visCtlOffsetMinHidden** <br/> |
| 8   <br/> | Décalé du centre, masqué  <br/> | Identique à 3 mais la poignée de contrôle n'est pas visible. |**visCtlOffsetMidHidden** <br/> |
| 9   <br/> | Décalé du bord droit, masqué  <br/> | Identique à 4 mais la poignée de contrôle n'est pas visible. |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y Behavior par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Contrôles.  *nom*  . Contrôles YConwhere.  *nom*  est le nom de la ligne des contrôles. |
   
Pour obtenir une référence à la cellule Y Behavior par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionControls** <br/> |
| **Index de la ligne :**  <br/> |**visRowControl** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visCtlYCon** <br/> |
   

