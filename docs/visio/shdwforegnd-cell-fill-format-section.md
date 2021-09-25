---
title: ShdwForegnd, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
ms.localizationpriority: medium
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Détermine la couleur du premier plan (traits) du motif de remplissage de l'ombre portée de la forme.
ms.openlocfilehash: 6f2d639a9df03d51c7d82dedd8cfbec2456a55db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598107"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>ShdwForegnd, cellule (section Fill Format)

Détermine la couleur du premier plan (traits) du motif de remplissage de l'ombre portée de la forme.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur, entrez une valeur comprise entre 0 et 23, correspondant à un index d’un ensemble de couleurs.
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB, et RVB( *r, g, b*), plutôt qu’un nombre, s’affiche dans la fenêtre Feuille ShapeSheet. Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24. 
  
Vous pouvez définir la transparence de la couleur de premier plan du motif de remplissage de l'ombre portée d'une forme dans la cellule ShdwForegndTrans.
  
Pour obtenir une référence à la cellule ShdwForegnd par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ShdwForegnd  <br/> |
   
Pour obtenir une référence à la cellule ShdwForegnd par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowFill** <br/> |
| Index de la cellule :  <br/> |**visFillShdwForegnd** <br/> |
   

