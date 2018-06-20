---
title: SortKey, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Correspond à une chaîne qui détermine l’ordre dans lequel les éléments dans la fenêtre données de forme sont répertoriés.
ms.openlocfilehash: 1dbc093f2cee509531b8148563fbdb1a777a349f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789797"
---
# <a name="sortkey-cell-shape-data-section"></a>SortKey, cellule (section Shape Data)

Correspond à une chaîne qui détermine l’ordre dans lequel les éléments dans la fenêtre **Données de forme** sont répertoriés. 
  
## <a name="remarks"></a>Remarques

Le calcul utilisé pour comparer les valeurs SortKey est spécifiques aux paramètres régionaux et de la casse. Si les valeurs SortKey sont égales, les données de forme sont répertoriées dans l’ordre des lignes. Données de forme qui n’ont aucune clé tri sont répertoriées après les données de forme qui contiennent une clé de tri.
  
Voici un exemple d’utilisation des clés de tri pour afficher les données de forme dans la fenêtre **Données de forme** dans l’ordre : numéro d’article, quantité, prix. 
  
 *Ligne, intitulé* et *SortKey* faire référence à des cellules dans la ligne de données de forme. Dans ce cas, les lignes de données de forme ont été nommés. 
  
|**Row**|**Étiquette**|**SortKey**|
|:-----|:-----|:-----|
| Prop.Item  <br/> | Référence article  <br/> | 1  <br/> |
| Prop.prix  <br/> | Prix  <br/> | 3  <br/> |
| Prop.Quan  <br/> | Quantité  <br/> | 2  <br/> |
   
Pour obtenir une référence à la cellule SortKey par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Propriétés.  *Nom* . SortKey où de propriétés.  *Nom* est le nom de la ligne de propriété personnalisée  <br/> |
   
Pour obtenir une référence à la cellule SortKey par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCustPropsSortKey** <br/> |
   

