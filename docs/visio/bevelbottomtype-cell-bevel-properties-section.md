---
title: BevelBottomType Cell (Bevel Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ac7b39d4-3942-4b23-b188-2c3f69e54929
description: Spécifie le type de biseau inférieur du biseau d'une forme.
ms.openlocfilehash: 0cd360f633145c7dea95438ffe2bc746e519ce13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330078"
---
# <a name="bevelbottomtype-cell-bevel-properties-section"></a>BevelBottomType Cell (Bevel Properties Section)

Spécifie le type de biseau inférieur du biseau d'une forme.
  
|**Value**|**Description**|
|:-----|:-----|
|0  <br/> |Aucun biseau  <br/> |
|0,1  <br/> |Biseau rond  <br/> |
|n°2  <br/> |Biseau reLâchée  <br/> |
|3  <br/> |Biseau  <br/> |
|4  <br/> |Biseau froid  <br/> |
|disque  <br/> |Biseau  <br/> |
|6.x  <br/> |Biseau arrondi  <br/> |
|7j/7  <br/> |Biseau convexe  <br/> |
|8bits  <br/> |Biseau pente  <br/> |
|4,9  <br/> |Biseau sillage  <br/> |
|10  <br/> |Biseau Riblet  <br/> |
|a4  <br/> |Biseau de côté dur  <br/> |
|an  <br/> |Biseau déco  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **BevelBottomType** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** au format de fichier. vsdx ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | BevelBottomType  <br/> |
   
Pour obtenir une référence à la cellule **BevelBottomType** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowBevelProperties** <br/> |
| Index de la cellule :  <br/> |**visBevelBottomType** <br/> |
   

