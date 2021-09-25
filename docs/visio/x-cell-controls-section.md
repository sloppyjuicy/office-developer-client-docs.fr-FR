---
title: X, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
ms.localizationpriority: medium
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: Représente la coordonnée x qui indique l’emplacement de la poignée de contrôle d’une forme dans les coordonnées locales.
ms.openlocfilehash: 948b27415d22f4beb2d4c6d0c3a14e53252920f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582519"
---
# <a name="x-cell-controls-section"></a>X, cellule (section Controls)

Représente la  *coordonnée x*  qui indique l’emplacement de la poignée de contrôle d’une forme dans les coordonnées locales. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Contrôles.  *nom*  . X où Controls.  *nom*  est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlX** <br/> |
   

