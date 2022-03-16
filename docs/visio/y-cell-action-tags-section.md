---
title: Y, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026934
ms.localizationpriority: medium
ms.assetid: b213fc46-7f80-99fd-60ba-8ddf3d0f6ee3
description: Position de la coordonnée y dans les coordonnées locales de la forme autour de laquelle le bouton de balise d’action est placé.
ms.openlocfilehash: 042d38e6e51960c4a69bd7aaf2e24b6cd64d6ee0
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507848"
---
# <a name="y-cell-action-tags-section"></a>Y, cellule (section Action Tags)

Position *de* la coordonnée y dans les coordonnées locales de la forme autour de laquelle le bouton de balise d’action est placé.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».
  
## <a name="remarks"></a>Remarques

Les cellules X et Y définissent un point dans le système de coordonnées locales de la forme, tandis que les cellules X Justify et Y Justify définissent le positionnement du bouton de balise d’action par rapport à ce point.
  
Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | SmartTags. *nom* . Y où SmartTags. *nom* est le nom de la ligne de balise d’action. <br/> |

Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionSmartTag** <br/> |
| **Index de la ligne :**  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visSmartTagY** <br/> |
