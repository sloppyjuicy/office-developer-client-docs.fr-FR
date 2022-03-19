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
ms.openlocfilehash: 40e9e0966036633c12228bca7f728f9958a68308
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627829"
---
# <a name="y-dynamics-cell-controls-section"></a>Y Dynamics, cellule (section Controls)

Représente la coordonnée  *y*  du point d’ancrage d’une poignée de contrôle dans les coordonnées locales. Le point d'ancrage est utilisé pour l'étirement dynamique des formes. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y Dynamics par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Contrôles.  *nameYDynwhere Controls.  *nom*  est le nom de la ligne des contrôles. |
   
Pour obtenir une référence à la cellule Y Dynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionControls** <br/> |
| **Index de la ligne :**  <br/> |**visRowControl** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visCtlYDyn** <br/> |
   

