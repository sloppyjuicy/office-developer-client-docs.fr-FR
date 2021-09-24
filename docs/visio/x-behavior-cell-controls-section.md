---
title: X Behavior, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251285
ms.localizationpriority: medium
ms.assetid: 82423d08-b6ce-0f23-8b61-354c3e5f323e
description: Contrôle le type de comportement de la coordonnée x de la poignée de contrôle une fois le handle déplacé.
ms.openlocfilehash: f9dcb76c9ad8dcea5ace2580e41daae83dd27a10
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549314"
---
# <a name="x-behavior-cell-controls-section"></a>X Behavior, cellule (section Controls)

Contrôle le type de comportement de  *la coordonnée x*  de la poignée de contrôle une fois le handle déplacé. 
  
|**Valeur**|**Comportement**|**Définition**|**Constante d'automation**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | Proportionnel  <br/> | La poignée de contrôle peut être déplacée et se déplace proportionnellement à la forme lorsque cette dernière est redimensionnée.  <br/> |**visCtlProportional** <br/> |
| 1  <br/> | Proportionnel verrouillé  <br/> | La poignée de contrôle se déplace proportionnellement à la forme lorsque cette dernière est redimensionnée mais ne peut être déplacée indépendamment de la forme.  <br/> |**visCtlLocked** <br/> |
| 2  <br/> | Décalé du bord gauche  <br/> | La poignée de contrôle est décalée d'une valeur constante par rapport au côté gauche de la forme.  <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> | Décalé du centre  <br/> | La poignée de contrôle est décalée d'une valeur constante par rapport au centre de la forme.  <br/> |**visCtlOffsetMid** <br/> |
| 4   <br/> | Décalé du bord droit  <br/> | La poignée de contrôle est décalée d'une valeur constante par rapport au côté droit de la forme.  <br/> |**visCtlOffsetMax** <br/> |
| 5  <br/> | Proportionnel, masqué  <br/> | Identique à 0 mais la poignée de contrôle n'est pas visible.  <br/> |**visCtlProportionalHidden** <br/> |
| 6   <br/> | Proportionnel verrouillé, masqué  <br/> | Identique à 1 mais la poignée de contrôle n'est pas visible.  <br/> |**visCtlLockedHiddenv** <br/> |
| 7   <br/> | Décalé du bord gauche, masqué  <br/> | Identique à 2 mais la poignée de contrôle n'est pas visible.  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8   <br/> | Décalé du centre, masqué  <br/> | Identique à 3 mais la poignée de contrôle n'est pas visible.  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9   <br/> | Décalé du bord droit, masqué  <br/> | Identique à 4 mais la poignée de contrôle n'est pas visible.  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule X Behavior par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrôles.  *nom*  . Contrôles XConwhere.  *nom*  est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule X Behavior par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlXCon** <br/> |
   

