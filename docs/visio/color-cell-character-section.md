---
title: Color, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Détermine la couleur utilisée pour le texte de la forme.
ms.openlocfilehash: ef07f4165882e08a2292e4ee549f8807fe8403e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788253"
---
# <a name="color-cell-character-section"></a>Color, cellule (section Character)

Détermine la couleur utilisée pour le texte de la forme.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur, tapez un nombre compris entre 0 et 23.
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB et RVB ( *r, g, b*), au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet. Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 24 et au-dessus. 
  
Vous pouvez définir une transparence pour la couleur du texte dans la cellule Transparency.
  
Pour obtenir une référence à la cellule Color par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Char.Color [ *i* ] où *i* = < 1 >, 2, 3,...  <br/> |
   
Pour obtenir une référence à la cellule Color par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2,...  <br/> |
|Index de la cellule :  <br/> |**visCharacterColor** <br/> |
   

