---
title: Y Behavior, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1190
localization_priority: Normal
ms.assetid: 6d5062d3-743b-8664-8ec9-5a8f11d5edf9
description: Contrôle le type de comportement de la coordonnée y de la poignée de contrôle une fois la poignée déplacée. Les formules suivantes sont disponibles.
ms.openlocfilehash: bf8cbd490884244c92b68784dcbf041093539c94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413576"
---
# <a name="y-behavior-cell-controls-section"></a>Y Behavior, cellule (section Controls)

Contrôle le type de comportement de la coordonnée  *y*  de la poignée de contrôle une fois la poignée déplacée. Les formules suivantes sont disponibles. 
  
|**Valeur**|**Comportement**|**Définition**|**Constante d'automation**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | Proportionnel  <br/> | La poignée de contrôle peut être déplacée et se déplace proportionnellement à la forme lorsque cette dernière est redimensionnée.  <br/> |**visCtlProportional** <br/> |
| 1  <br/> | Proportionnel verrouillé  <br/> | La poignée de contrôle se déplace proportionnellement à la forme lorsque cette dernière est redimensionnée mais ne peut être déplacée indépendamment de la forme.  <br/> |**visCtlLocked** <br/> |
| 2  <br/> | Décalé du bord inférieur  <br/> | La poignée de contrôle est décalée d'une valeur constante par rapport au bas de la forme.  <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> | Décalé du centre  <br/> | La poignée de contrôle est décalée d'une valeur constante par rapport au centre de la forme.  <br/> |**visCtlOffsetMid** <br/> |
| 4   <br/> | Décalé du bord supérieur  <br/> | La poignée de contrôle est décalée d'une valeur constante par rapport au haut de la forme.  <br/> |**visCtlOffsetMax** <br/> |
| 5   <br/> | Proportionnel, masqué  <br/> | Identique à 0 mais la poignée de contrôle n'est pas visible.  <br/> |**visCtlProportionalHidden** <br/> |
| 6   <br/> | Proportionnel verrouillé, masqué  <br/> | Identique à 1 mais la poignée de contrôle n'est pas visible.  <br/> |**visCtlLockedHiddenv** <br/> |
| 7   <br/> | Décalé du bord gauche, masqué  <br/> | Identique à 2 mais la poignée de contrôle n'est pas visible.  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8   <br/> | Décalé du centre, masqué  <br/> | Identique à 3 mais la poignée de contrôle n'est pas visible.  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9   <br/> | Décalé du bord droit, masqué  <br/> | Identique à 4 mais la poignée de contrôle n'est pas visible.  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y Behavior par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrôles.  *nom*  . Contrôles YConwhere.  *nom*  est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule Y Behavior par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlYCon** <br/> |
   

