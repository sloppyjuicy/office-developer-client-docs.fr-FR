---
title: Tip, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
ms.localizationpriority: medium
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: Représente une chaîne de description qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme. L'application affiche automatiquement ces informations détaillées entre guillemets dans la cellule. Ces guillemets n'apparaissent pas dans l'info-bulle.
ms.openlocfilehash: eb0356af6da6a712b7cf284f833401b103e39379
ms.sourcegitcommit: bebcc8c6f480997f9dfa5c476daf62249b8791f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2021
ms.locfileid: "61558883"
---
# <a name="tip-cell-controls-section"></a>Tip, cellule (section Controls)

Représente une chaîne de description qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme. L'application affiche automatiquement ces informations détaillées entre guillemets dans la cellule. Ces guillemets n'apparaissent pas dans l'info-bulle.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Tip par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrôles. *nom* . Invite où contrôles.  *nom*  est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule Tip par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlTip** <br/> |
   

