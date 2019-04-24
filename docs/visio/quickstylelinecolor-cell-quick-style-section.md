---
title: QuickStyleLineColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: Détermine la couleur de thème utilisée par la ligne d'une forme, sous la forme d'un nombre entier compris entre 0 et 7.
ms.openlocfilehash: 010b943f2266b1e0ee192e5f1341d73851d176fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360047"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a>QuickStyleLineColor Cell (Quick Style Section)

Détermine la couleur de thème utilisée par la ligne d'une forme, sous la forme d'un nombre entier compris entre 0 et 7.
  
|||
|:-----|:-----|
|Valeur  <br/> |Description  <br/> |
|0  <br/> |La couleur de trait de la forme hérite de la couleur de thème foncé.  <br/> |
|0,1  <br/> |La couleur de trait de la forme hérite de la couleur de thème clair.  <br/> |
|n°2  <br/> |La couleur de trait de la forme hérite de la couleur de thème accent 1  <br/> |
|3  <br/> |La couleur de trait de la forme hérite de la couleur de thème accent 2  <br/> |
|4  <br/> |La couleur de trait de la forme hérite de la couleur de thème accent 3  <br/> |
|disque  <br/> |La couleur de trait de la forme hérite de la couleur de thème accent 4  <br/> |
|6.x  <br/> |La couleur de trait de la forme hérite de la couleur de thème accent 5  <br/> |
|7j/7  <br/> |La couleur de trait de la forme hérite de la couleur de thème accent 6  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **QuickStyleLineColor** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | QuickStyleLineColor  <br/> |
   
Pour obtenir une référence à la cellule **QuickStyleLineColor** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowQuickStyleProperties** <br/> |
| Index de la cellule :  <br/> |**visQuickStyleLineColor** <br/> |
   

