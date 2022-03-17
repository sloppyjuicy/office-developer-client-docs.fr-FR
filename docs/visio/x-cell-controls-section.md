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
ms.openlocfilehash: cb9f8345d1df61102a1b3410f1ed577f404bde6e
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521098"
---
# <a name="x-cell-controls-section"></a>X, cellule (section Controls)

Représente la coordonnée  *x*  qui indique l’emplacement de la poignée de contrôle d’une forme dans les coordonnées locales. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Contrôles.  *nom*  . X où Controls.  *nom*  est le nom de la ligne des contrôles. |
   
Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionControls** <br/> |
| **Index de la ligne :**  <br/> |**visRowControl** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visCtlX** <br/> |
   

