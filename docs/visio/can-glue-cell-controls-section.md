---
title: Can Glue, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
ms.localizationpriority: medium
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Détermine si une poignée de contrôle peut être collée à d'autres formes.
ms.openlocfilehash: 138939c676013948ba7644ebec9dfcba10db87c8
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63519845"
---
# <a name="can-glue-cell-controls-section"></a>Can Glue, cellule (section Controls)

Détermine si une poignée de contrôle peut être collée à d'autres formes.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La poignée de contrôle peut être collée. |
| FALSE  <br/> | La poignée de contrôle ne peut pas être collée. |

## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Can Glue par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Contrôles. *nom* . Contrôles CanGluewhere. *Nom* est le nom de la ligne des contrôles. |

Pour obtenir une référence à la cellule Can Glue à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionControls** <br/> |
| **Index de la ligne :**  <br/> |**visRowControl** +   *i* où *i* = 0, 1, 2, ... |
| **Index de la cellule :**  <br/> |**visCtlGlue** <br/> |
