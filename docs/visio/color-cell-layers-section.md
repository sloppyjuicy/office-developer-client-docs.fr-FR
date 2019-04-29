---
title: Color, cellule (section Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Indique la couleur utilisée pour afficher le calque.
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435130"
---
# <a name="color-cell-layers-section"></a>Color, cellule (section Layers)

Indique la couleur utilisée pour afficher le calque.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur, tapez un nombre compris entre 0 et 23.
  
Cette valeur de cellule correspond au **paramètre couleur de calque** dans la boîte de dialogue Propriétés des **calques** (dans le groupe **modification** de l'onglet **Accueil** , cliquez sur **calques** , puis sur Propriétés des **calques**).
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d'une couleur personnalisée est sa couleur RVB et la valeur RVB ( *r, v, b*), au lieu d'un nombre, est affichée dans la fenêtre feuille ShapeSheet. Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24. Une valeur de 255 indique que le calque n'a pas de couleur. 
  
Vous pouvez définir la transparence de la couleur du calque dans la cellule Transparency.
  
Pour obtenir une référence à la cellule Color par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Layers. Color [ *i* ] où *i* = <1>, 2, 3,...  <br/> |
   
Pour obtenir une référence à la cellule Color à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +  *i* où *i* = 0, 1, 2,...  <br/> |
|Index de la cellule :  <br/> |**visLayerColor** <br/> |
   

