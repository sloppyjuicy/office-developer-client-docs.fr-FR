---
title: DontMoveChildren, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
ms.localizationpriority: medium
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Détermine la possibilité ou non de faire glisser, à l'aide de la souris, des formes dans un groupe.
ms.openlocfilehash: a33a747849ce9918b9d1436098211e404f4087bb
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63523513"
---
# <a name="dontmovechildren-cell-group-properties-section"></a>DontMoveChildren, cellule (section Group Properties)

Détermine la possibilité ou non de faire glisser, à l'aide de la souris, des formes dans un groupe.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Les formes d'un groupe ne peuvent pas être déplacées avec la souris. |
| FALSE  <br/> | Les formes d'un groupe peuvent être déplacées avec la souris. |
   
## <a name="remarks"></a>Remarques

Lorsque cette cellule est réglée sur TRUE, vous pouvez retourner, faire pivoter, redimensionner ou repositionner les formes d'un groupe à l'aide des autres méthodes.
  
Cette cellule a pour valeur TRUE pour les groupes de formes de base et ceux d'instances de formes de base créées avec les versions de Visio antérieures à Visio 2000.
  
Pour obtenir une référence à la cellule DontMoveChildren par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | DontMoveChildren  <br/> |
   
Pour obtenir une référence à la cellule DontMoveChildren à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowGroup** <br/> |
| **Index de la cellule :**  <br/> |**visGroupDontMoveChildren** <br/> |
   

