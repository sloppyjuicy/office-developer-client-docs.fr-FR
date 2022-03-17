---
title: Y, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
ms.localizationpriority: medium
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Représente la coordonnée y qui indique l’emplacement de la poignée de contrôle d’une forme dans les coordonnées locales.
ms.openlocfilehash: 1a7a11f0fc5ed073653aeaf8a16e5635ea8d946d
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520604"
---
# <a name="y-cell-controls-section"></a>Y, cellule (section Controls)

Représente la coordonnée *y* qui indique l’emplacement de la poignée de contrôle d’une forme dans les coordonnées locales.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Contrôles.  *nom* . Y où Contrôles. *Nom* est le nom de la ligne des contrôles. |

Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionControls** <br/> |
| **Index de la ligne :**  <br/> |**visRowControl** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visCtlY** <br/> |
