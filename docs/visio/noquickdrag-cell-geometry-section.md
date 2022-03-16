---
title: NoQuickDrag, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
ms.localizationpriority: medium
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Détermine si une forme peut être sélectionnée ou glissée lorsque l’utilisateur clique sur la zone remplie définie par la section Geometry.
ms.openlocfilehash: b831e94ef0d644f9ad8df97f443cc2e4bbf63c51
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506733"
---
# <a name="noquickdrag-cell-geometry-section"></a>NoQuickDrag, cellule (section Geometry)

Détermine si une forme peut être sélectionnée ou glissée lorsque l’utilisateur clique sur la zone remplie définie par la section Geometry.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule NoQuickDrag par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Geometry  *i*  . NoQuickDrag, où  *i* - <1>, 2, 3... |

Pour obtenir une référence à la cellule NoQuickDrag à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionFirstComponent** +  *i*, où *i* = 0, 1, 2... |
|**Index de la ligne :**  <br/> |**visRowComponent** <br/> |
|**Index de la cellule :**  <br/> |**visCompNoQuickDrag** <br/> |
