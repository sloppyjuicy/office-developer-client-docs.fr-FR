---
title: Color, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
ms.localizationpriority: medium
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Détermine la couleur utilisée pour le texte de la forme.
ms.openlocfilehash: bff5857a8351004304e75b6000e2937372f9e905
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608486"
---
# <a name="color-cell-character-section"></a>Color, cellule (section Character)

Détermine la couleur utilisée pour le texte de la forme.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur, tapez un nombre compris entre 0 et 23.
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB, et RVB( *r, g, b*), plutôt qu’un nombre, s’affiche dans la fenêtre Feuille ShapeSheet. Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24. 
  
Vous pouvez définir une transparence pour la couleur du texte dans la cellule Transparency.
  
Pour obtenir une référence à la cellule Color par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Char.Color[ *i*  ] où  *i*  = <1>, 2, 3, ...  <br/> |
   
Pour obtenir une référence à la cellule Color à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionCharacter** <br/> |
|Index de la ligne :  <br/> |**visRowCharacter**  +   *i* où *i* = 0, 1, 2, ...  <br/> |
|Index de la cellule :  <br/> |**visCharacterColor** <br/> |
   

