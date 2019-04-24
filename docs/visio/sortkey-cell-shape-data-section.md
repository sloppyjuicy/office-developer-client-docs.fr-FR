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
description: Produit une chaîne qui détermine l’ordre dans lequel les éléments de la fenêtre Données de forme sont présentés.
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335181"
---
# <a name="sortkey-cell-shape-data-section"></a>SortKey, cellule (section Shape Data)

Produit une chaîne qui détermine l’ordre dans lequel les éléments de la fenêtre **Données de forme** sont présentés. 
  
## <a name="remarks"></a>Remarques

Le calcul utilisé pour comparer les valeurs SortKey est basé sur les paramètres régionaux spécifiques et ne tient pas compte des majuscules et des minuscules. Si les valeurs SortKey sont égales, les données de forme sont présentées dans l'ordre des lignes. Les données de forme qui n'ont pas de clé de tri sont répertoriées après les données de forme qui contiennent une clé de tri.
  
Entrez par exemple les clés de tri suivantes pour afficher les données de forme dans la fenêtre **Données de forme** dans l’ordre Référence article, Quantité, Prix. 
  
 *Ligne, étiquette* et *SortKey* font référence à des cellules de la ligne de données de forme. Dans ce cas, les lignes de données de forme ont été nommées. 
  
|**Ligne**|**Label**|**SortKey**|
|:-----|:-----|:-----|
| Prop. Item  <br/> | Référence article  <br/> | 0,1  <br/> |
| Prop. Price  <br/> | Price  <br/> | 3  <br/> |
| Prop. Quan  <br/> | Quantité  <br/> | n°2  <br/> |
   
Pour obtenir une référence à la cellule SortKey par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Hélice.  *Nom* . SortKey Where.  *Name* est le nom de la ligne de la propriété personnalisée.  <br/> |
   
Pour obtenir une référence à la cellule SortKey par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCustPropsSortKey** <br/> |
   

