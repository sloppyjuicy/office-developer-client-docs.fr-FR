---
title: ThemeIndex Cell (Theme Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Stocke l'énumération du thème Microsoft Visio intégré appliqué au document, sous la forme d'un nombre entier. Lorsqu'un nouveau thème est choisi pour le document, la cellule ThemeIndex du document et toutes les pages et formes qu'il contient sont mises à jour avec l'index du thème intégré.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360528"
---
# <a name="themeindex-cell-theme-properties-section"></a>ThemeIndex Cell (Theme Properties Section)

Stocke l'énumération du thème Microsoft Visio intégré appliqué au document, sous la forme d'un nombre entier. Lorsqu'un nouveau thème est choisi pour le document, la cellule **ThemeIndex** du document et toutes les pages et formes qu'il contient sont mises à jour avec l'index du thème intégré. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **ThemeIndex** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ThemeIndex  <br/> |
   
Pour obtenir une référence à la cellule **ThemeIndex** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowThemeProperties** <br/> |
| Index de la cellule :  <br/> |**visThemeIndex** <br/> |
   

