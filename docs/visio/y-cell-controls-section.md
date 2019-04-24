---
title: Y, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Représente la coordonnée y qui indique l'emplacement de la poignée de contrôle d'une forme en coordonnées locales.
ms.openlocfilehash: 14aaa7aef7e7250baeb8ffb863244ece26a201e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360150"
---
# <a name="y-cell-controls-section"></a>Y, cellule (section Controls)

Représente la coordonnée *y* qui indique l'emplacement de la poignée de contrôle d'une forme en coordonnées locales. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Vérifie.  *nom* . Contrôles Yoù.  *Name* est le nom de la ligne Controls.  <br/> |
   
Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlY** <br/> |
   

