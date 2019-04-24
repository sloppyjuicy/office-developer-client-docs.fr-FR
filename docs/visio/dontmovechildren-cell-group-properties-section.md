---
title: DontMoveChildren, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Détermine la possibilité ou non de faire glisser, à l'aide de la souris, des formes dans un groupe.
ms.openlocfilehash: 2b15d75a98b5f5a72bce8b80758d27b197a346ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338583"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>DontMoveChildren, cellule (section Group Properties)

Détermine la possibilité ou non de faire glisser, à l'aide de la souris, des formes dans un groupe.
  
|**Value**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Les formes d'un groupe ne peuvent pas être déplacées avec la souris.  <br/> |
| FALSE  <br/> | Les formes d'un groupe peuvent être déplacées avec la souris.  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque cette cellule est réglée sur TRUE, vous pouvez retourner, faire pivoter, redimensionner ou repositionner les formes d'un groupe à l'aide des autres méthodes.
  
Cette cellule a pour valeur TRUE pour les groupes de formes de base et ceux d'instances de formes de base créées avec les versions de Visio antérieures à Visio 2000.
  
Pour obtenir une référence à la cellule DontMoveChildren par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | DontMoveChildren  <br/> |
   
Pour obtenir une référence à la cellule DontMoveChildren à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowGroup** <br/> |
| Index de la cellule :  <br/> |**visGroupDontMoveChildren** <br/> |
   

