---
title: FillBkgnd, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
ms.localizationpriority: medium
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Détermine la couleur d'arrière-plan (remplissage) du motif de remplissage de la forme.
ms.openlocfilehash: 2b4c204eb206c32889e3b7a1683261e5fca33bb1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582735"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>FillBkgnd, cellule (section Fill Format)

Détermine la couleur d'arrière-plan (remplissage) du motif de remplissage de la forme.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur, tapez un nombre compris entre 0 et 23.
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d'une couleur personnalisée est sa valeur RVB et la fenêtre Feuille ShapeSheet affiche RVB (*r, v, b*) au lieu d'une valeur. Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24. 
  
Vous pouvez définir la transparence de remplissage de l'arrière-plan dans la cellule FillBkgndTrans. 
  
Pour obtenir une référence à la cellule FillBkgnd par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | FillBkgnd  <br/> |
   
Pour obtenir une référence à la cellule FillBkgnd à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowFill** <br/> |
| Index de la cellule :  <br/> |**visFillBkgnd** <br/> |
   

