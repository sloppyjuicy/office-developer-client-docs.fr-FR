---
title: X Dynamics, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Représente la coordonnée x du point d'ancrage d'une poignée de contrôle, exprimée dans le système de coordonnées locales.
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322301"
---
# <a name="x-dynamics-cell-controls-section"></a>X Dynamics, cellule (section Controls)

Représente la coordonnée *x* du point d'ancrage d'une poignée de contrôle, exprimée dans le système de coordonnées locales. 
  
## <a name="remarks"></a>Remarques

Le point d'ancrage est utilisé pour l'étirement dynamique des formes.
  
Pour obtenir une référence à la cellule X Dynamics par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Vérifie.  *nom* . Contrôles XDynwhere.  *Name* est le nom de la ligne Controls.  <br/> |
   
Pour obtenir une référence à la cellule X Dynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlXDyn** <br/> |
   

