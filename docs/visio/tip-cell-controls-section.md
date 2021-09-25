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
ms.openlocfilehash: 834583eece5c71d42218e67411944fee11279f65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569887"
---
# <a name="tip-cell-controls-section"></a>Tip, cellule (section Controls)

Représente une chaîne de description qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme. L'application affiche automatiquement ces informations détaillées entre guillemets dans la cellule. Ces guillemets n'apparaissent pas dans l'info-bulle.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Tip par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrôles.  *nom*  . Tipwhere Controls.  *nom*  est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule Tip par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlTip** <br/> |
   

