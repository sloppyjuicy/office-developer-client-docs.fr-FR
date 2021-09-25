---
title: Y Dynamics, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
ms.localizationpriority: medium
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Représente la coordonnée y du point d’ancrage d’une poignée de contrôle dans les coordonnées locales. Le point d'ancrage est utilisé pour l'étirement dynamique des formes.
ms.openlocfilehash: 0e60b9e2233068bc950d4649ff261dcc92e8e1a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581741"
---
# <a name="y-dynamics-cell-controls-section"></a>Y Dynamics, cellule (section Controls)

Représente la coordonnée  *y*  du point d’ancrage d’une poignée de contrôle dans les coordonnées locales. Le point d'ancrage est utilisé pour l'étirement dynamique des formes. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y Dynamics par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrôles.  *nom*  . Contrôles YDynwhere.  *nom*  est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule Y Dynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlYDyn** <br/> |
   

