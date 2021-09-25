---
title: X Dynamics, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
ms.localizationpriority: medium
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Représente la coordonnée x du point d’ancrage d’une poignée de contrôle dans les coordonnées locales.
ms.openlocfilehash: 9389d8e0974a5f89bfc4eee18b107dab5b0c25ca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559331"
---
# <a name="x-dynamics-cell-controls-section"></a>X Dynamics, cellule (section Controls)

Représente la coordonnée  *x*  du point d’ancrage d’une poignée de contrôle dans les coordonnées locales. 
  
## <a name="remarks"></a>Remarques

Le point d'ancrage est utilisé pour l'étirement dynamique des formes.
  
Pour obtenir une référence à la cellule X Dynamics par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrôles.  *nom*  . Contrôles XDynwhere.  *nom*  est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule X Dynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlXDyn** <br/> |
   

