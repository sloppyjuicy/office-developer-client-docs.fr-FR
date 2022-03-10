---
title: FillForegnd, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
ms.localizationpriority: medium
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Détermine la couleur du premier plan (traits) du motif de remplissage de la forme.
ms.openlocfilehash: caee830f45469f7827d4a77ca7e8c6ee0332ba47
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426649"
---
# <a name="fillforegnd-cell-fill-format-section"></a>FillForegnd, cellule (section Fill Format)

Détermine la couleur du premier plan (traits) du motif de remplissage de la forme.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur, tapez un nombre compris entre 0 et 23.
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB, et RVB( *r, g, b*), au lieu d’un nombre, s’affiche dans la fenêtre Feuille ShapeSheet. Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24. 
  
Vous pouvez définir la transparence de remplissage de premier plan dans la cellule TransPremPlanRempl.
  
Pour obtenir une référence à la cellule FillForegnd par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |FillForegnd  <br/> |
   
Pour obtenir une référence à la cellule FillForegnd à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowFill** <br/> |
|**Index de la cellule :**  <br/> |**visFillForegnd** <br/> |
   

