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
ms.openlocfilehash: 5a0f927b313ca6457cc4bc2a8745b3c1dd6b245c
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63633630"
---
# <a name="x-dynamics-cell-controls-section"></a>X Dynamics, cellule (section Controls)

Représente la coordonnée  *x*  du point d’ancrage d’une poignée de contrôle dans les coordonnées locales. 
  
## <a name="remarks"></a>Remarques

Le point d'ancrage est utilisé pour l'étirement dynamique des formes.
  
Pour obtenir une référence à la cellule X Dynamics par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Contrôles.  *nom*  . Contrôles XDynwhere.  *nom*  est le nom de la ligne des contrôles. |
   
Pour obtenir une référence à la cellule X Dynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionControls** <br/> |
| **Index de la ligne :**  <br/> |**visRowControl** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visCtlXDyn** <br/> |
   

