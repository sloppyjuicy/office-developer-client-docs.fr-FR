---
title: X, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
ms.localizationpriority: medium
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: Position de coordonnée x dans les coordonnées locales de la forme autour de laquelle le bouton de balise d’action est placé.
ms.openlocfilehash: e4a4921abef1f16e7ca883bda4d258dc818f60d4
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633644"
---
# <a name="x-cell-action-tags-section"></a>X, cellule (section Action Tags)

Position *de coordonnée x*  dans les coordonnées locales de la forme autour de laquelle le bouton de balise d’action est placé. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Remarques

Les cellules X et Y définissent un point dans le système de coordonnées locales de la forme, tandis que les cellules X Justify et Y Justify définissent le positionnement du bouton de balise d’action par rapport à ce point. 
  
Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> |SmartTags. *nom*  . X où SmartTags. *name est*  le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionSmartTag** <br/> |
| **Index de la ligne :**  <br/> |**visRowSmartTag** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visSmartTagX** <br/> |
   

