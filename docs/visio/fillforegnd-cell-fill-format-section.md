---
title: FillForegnd, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Détermine la couleur du premier plan (traits) du motif de remplissage de la forme.
ms.openlocfilehash: 27126457963e4e55419b0cac5baf1eab08fe3cc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788638"
---
# <a name="fillforegnd-cell-fill-format-section"></a>FillForegnd, cellule (section Fill Format)

Détermine la couleur du premier plan (traits) du motif de remplissage de la forme.
  
## <a name="remarks"></a>Note

Pour définir la couleur, tapez un nombre compris entre 0 et 23.
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB et RVB ( *r, g, b*), au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet. Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 24 et au-dessus. 
  
Vous pouvez définir la transparence de remplissage de premier plan dans la cellule TransPremPlanRempl.
  
Pour obtenir une référence à la cellule FillForegnd par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |FillForegnd  <br/> |
   
Pour obtenir une référence à la cellule FillForegnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillForegnd** <br/> |
   

