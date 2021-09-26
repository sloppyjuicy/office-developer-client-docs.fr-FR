---
title: LineColor, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
ms.localizationpriority: medium
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Détermine la couleur de trait de la forme.
ms.openlocfilehash: 8b3381ead5299420b429cc200daa0450f3f0c0a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618671"
---
# <a name="linecolor-cell-line-format-section"></a>LineColor, cellule (section Line Format)

Détermine la couleur de trait de la forme.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur de trait, entrez un nombre compris entre 0 et 23. Il s’agit d’un index d’un ensemble de couleurs de trait. Vous pouvez afficher l’ensemble de couleurs de trait dans la boîte de dialogue **Trait** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Trait**, pointez sur **Poids**, puis cliquez sur **Autres traits**). Vous pouvez également définir la valeur de LineColor dans la boîte de dialogue **Trait**. 
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB, et RVB( *r, g, b*), plutôt qu’un nombre, s’affiche dans la fenêtre Feuille ShapeSheet. Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24. 
  
Vous pouvez définir la transparence de la couleur du trait dans la cellule LineColorTrans.
  
Pour obtenir une référence à la cellule LineColor par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LineColor  <br/> |
   
Pour obtenir une référence à la cellule LineColor à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLine** <br/> |
|Index de la cellule :  <br/> |**visLineColor** <br/> |
   

