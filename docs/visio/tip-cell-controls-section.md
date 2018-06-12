---
title: Tip, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
localization_priority: Normal
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: Représente une chaîne de description qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme. L'application affiche automatiquement ces informations détaillées entre guillemets dans la cellule. Ces guillemets n'apparaissent pas dans l'info-bulle.
ms.openlocfilehash: ff593ee95dc27ba7192ee31d35791127b666eac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789910"
---
# <a name="tip-cell-controls-section"></a>Tip, cellule (section Controls)

Représente une chaîne de description qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme. L'application affiche automatiquement ces informations détaillées entre guillemets dans la cellule. Ces guillemets n'apparaissent pas dans l'info-bulle.
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Tip par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrôles.  *nom* . Contrôles Tipwhere.  *nom* est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule Tip par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlTip** <br/> |
   

