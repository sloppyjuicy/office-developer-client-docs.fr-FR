---
title: ThemeIndex, cellule (Section Propriétés de thème)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Stocke l’énumération du thème Microsoft Visio intégrée appliquée au document, comme un entier. Lorsque vous choisissez un nouveau thème pour le document, la cellule ThemeIndex pour le document et toutes les pages et les formes qu’il contient est mis à jour avec l’index du thème intégré.
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789882"
---
# <a name="themeindex-cell-theme-properties-section"></a>ThemeIndex, cellule (Section Propriétés de thème)

Stocke l’énumération du thème Microsoft Visio intégrée appliquée au document, comme un entier. Lorsque vous choisissez un nouveau thème pour le document, la cellule **ThemeIndex** pour le document et toutes les pages et les formes qu’il contient est mis à jour avec l’index du thème intégré. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **ThemeIndex** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ThemeIndex  <br/> |
   
Pour obtenir une référence à la cellule **ThemeIndex** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowThemeProperties** <br/> |
| Index de la cellule :  <br/> |**visThemeIndex** <br/> |
   

