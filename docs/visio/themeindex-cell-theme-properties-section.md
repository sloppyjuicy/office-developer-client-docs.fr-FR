---
title: ThemeIndex Cell (Theme Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Stocke l’éumération du thème Microsoft Visio intégré appliqué au document, sous la mesure d’un nombre. Lorsqu’un nouveau thème est choisi pour le document, la cellule ThemeIndex du document et toutes les pages et formes qu’il contient est mise à jour avec l’index du thème intégré.
ms.openlocfilehash: 2c79bb1a7d8197deb8bc5f4d1d6b79d1d7898a8e
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627955"
---
# <a name="themeindex-cell-theme-properties-section"></a>ThemeIndex Cell (Theme Properties Section)

Stocke l’éumération du thème Microsoft Visio intégré appliqué au document, sous la mesure d’un nombre. Lorsqu’un nouveau thème est choisi pour le document, la cellule **ThemeIndex** du document et toutes les pages et formes qu’il contient est mise à jour avec l’index du thème intégré. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **ThemeIndex** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | ThemeIndex  <br/> |
   
Pour obtenir une référence à la **cellule ThemeIndex** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowThemeProperties** <br/> |
| **Index de la cellule :**  <br/> |**visThemeIndex** <br/> |
   

