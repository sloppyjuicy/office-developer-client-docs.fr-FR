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
ms.openlocfilehash: b6728d44c71f6403e772a6a7e730ba3c18d9eb48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788270"
---
# <a name="color-cell-layers-section"></a>Color, cellule (section Layers)

Indique la couleur utilisée pour afficher le calque.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur, tapez un nombre compris entre 0 et 23.
  
Valeur de cette cellule correspond au paramètre **couleur de calque** dans la boîte de dialogue **Propriétés des calques** (dans le groupe **modification** , sous l’onglet **accueil** , cliquez sur **calques** , puis cliquez sur **Propriétés des calques**).
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB et RVB ( *r, g, b*), au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet. Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 24 et au-dessus. Une valeur de 255 indique que le calque n’a aucune couleur. 
  
Vous pouvez définir la transparence de la couleur du calque dans la cellule Transparency.
  
Pour obtenir une référence à la cellule Color par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Layers.Color [ *i* ] où *i* = < 1 >, 2, 3,...  <br/> |
   
Pour obtenir une référence à la cellule Color par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionLayer** <br/> |
|Index de la ligne :  <br/> |**visRowLayer** +  *i* où *i* = 0, 1, 2,...  <br/> |
|Index de la cellule :  <br/> |**visLayerColor** <br/> |
   

