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
ms.openlocfilehash: 11a4266b197a489e6ff68d18653b8cc4d4b195e0
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426656"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>FillBkgnd, cellule (section Fill Format)

Détermine la couleur d'arrière-plan (remplissage) du motif de remplissage de la forme.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur, tapez un nombre compris entre 0 et 23.
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d'une couleur personnalisée est sa valeur RVB et la fenêtre Feuille ShapeSheet affiche RVB (*r, v, b*) au lieu d'une valeur. Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24. 
  
Vous pouvez définir la transparence de remplissage de l'arrière-plan dans la cellule FillBkgndTrans. 
  
Pour obtenir une référence à la cellule FillBkgnd par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | FillBkgnd  <br/> |
   
Pour obtenir une référence à la cellule FillBkgnd à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowFill** <br/> |
| **Index de la cellule :**  <br/> |**visFillBkgnd** <br/> |
   

