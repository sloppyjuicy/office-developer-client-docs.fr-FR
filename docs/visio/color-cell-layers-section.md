---
title: Color, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
ms.localizationpriority: medium
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Indique la couleur utilisée pour afficher le calque.
ms.openlocfilehash: a996568875e4064aabe0198de8be15aa6798377e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783543"
---
# <a name="color-cell-layers-section"></a>Color, cellule (section Layers)

Indique la couleur utilisée pour afficher le calque.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur, tapez un nombre compris entre 0 et 23.
  
Cette valeur de cellule correspond au paramètre de couleur Layer dans la  boîte de dialogue Propriétés des calques (dans le groupe  Édition de l’onglet Accueil, cliquez sur Calques, puis sur Propriétés des **calques**).  
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB, et RVB( *r, g, b*), au lieu d’un nombre, s’affiche dans la fenêtre Feuille ShapeSheet. Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24. Une valeur de 255 indique que le calque n'a pas de couleur. 
  
Vous pouvez définir la transparence de la couleur du calque dans la cellule Transparency.
  
Pour obtenir une référence à la cellule Color par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Layers.Color[ *i*  ] où  *i*  = <1>, 2, 3, ... |
   
Pour obtenir une référence à la cellule Color à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +   *i* où *i* = 0, 1, 2, ... |
|Index de la cellule :  <br/> |**visLayerColor** <br/> |
   

