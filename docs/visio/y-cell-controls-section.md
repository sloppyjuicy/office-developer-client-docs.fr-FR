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
ms.openlocfilehash: 0b80ed8ad95c320197ea2f2b48f2bf14a87c8422
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374823"
---
# <a name="y-cell-controls-section"></a>Y, cellule (section Controls)

Représente la coordonnée *y* qui indique l’emplacement de la poignée de contrôle d’une forme dans les coordonnées locales.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Contrôles.  *nom* . Y où Contrôles. *Nom* est le nom de la ligne des contrôles. |

Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visCtlY** <br/> |
