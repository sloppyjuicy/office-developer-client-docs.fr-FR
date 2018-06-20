---
title: QuickStyleType, cellule (Section Style rapide)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Détermine le type de Style rapide (2D, 1D, ou le connecteur) qui hérite de la forme.
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789383"
---
# <a name="quickstyletype-cell-quick-style-section"></a>QuickStyleType, cellule (Section Style rapide)

Détermine le type de Style rapide (2D, 1D, ou le connecteur) qui hérite de la forme. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Visio choisit automatiquement  <br/> |
|1  <br/> |1D  <br/> |
|2  <br/> |2D  <br/> |
|3  <br/> |Connecteur  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **QuickStyleType** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | QuickStyleType  <br/> |
   
Pour obtenir une référence à la cellule **QuickStyleType** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowQuickStyleProperties** <br/> |
| Index de la cellule :  <br/> |**visQuickStyleType** <br/> |
   

