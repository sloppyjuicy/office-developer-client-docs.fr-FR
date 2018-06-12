---
title: ShdwForegnd, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Détermine la couleur du premier plan (traits) du motif de remplissage de l'ombre portée de la forme.
ms.openlocfilehash: f39109a296949d23142017661bb55f0708402d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789708"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>ShdwForegnd, cellule (section Fill Format)

Détermine la couleur du premier plan (traits) du motif de remplissage de l'ombre portée de la forme.
  
## <a name="remarks"></a>Note

Pour définir la couleur, entrez une valeur comprise entre 0 et 23, correspondant à un index d’un ensemble de couleurs.
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB et RVB ( *r, g, b*), au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet. Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 24 et au-dessus. 
  
Vous pouvez définir la transparence de la couleur de premier plan du motif de remplissage de l'ombre portée d'une forme dans la cellule ShdwForegndTrans.
  
Pour obtenir une référence à la cellule ShdwForegnd par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ShdwForegnd  <br/> |
   
Pour obtenir une référence à la cellule ShdwForegnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowFill** <br/> |
| Index de la cellule :  <br/> |**visFillShdwForegnd** <br/> |
   

