---
title: FillBkgnd, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: Détermine la couleur d'arrière-plan (remplissage) du motif de remplissage de la forme.
ms.openlocfilehash: d1222026887313d7737a3a0ded9e798e9bf5ea30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788617"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>FillBkgnd, cellule (section Fill Format)

Détermine la couleur d'arrière-plan (remplissage) du motif de remplissage de la forme.
  
## <a name="remarks"></a>Note

Pour définir la couleur, tapez un nombre compris entre 0 et 23.
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB et RVB (*r, g, b*), au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet. Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 24 et au-dessus. 
  
Vous pouvez définir la transparence de remplissage de l'arrière-plan dans la cellule FillBkgndTrans. 
  
Pour obtenir une référence à la cellule FillBkgnd par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | FillBkgnd  <br/> |
   
Pour obtenir une référence à la cellule FillBkgnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowFill** <br/> |
| Index de la cellule :  <br/> |**visFillBkgnd** <br/> |
   

