---
title: LineColor, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Détermine la couleur de trait de la forme.
ms.openlocfilehash: 6086a45108b88475e250c4d833ab4b740f33b8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788951"
---
# <a name="linecolor-cell-line-format-section"></a>LineColor, cellule (section Line Format)

Détermine la couleur de trait de la forme.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur de trait, entrez un nombre entre 0 et 23, qui est un index dans une collection de couleurs. Vous pouvez afficher l’ensemble de couleur de trait dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **poids**, puis cliquez sur **Autres traits**). Vous pouvez également définir la valeur de LineColor dans la boîte de dialogue **trait** . 
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB et RVB ( *r, g, b*), au lieu d’un nombre, s’affichera dans la fenêtre feuille ShapeSheet. Lorsqu’il est utilisé dans les opérations numériques, les couleurs personnalisées ont des valeurs de 24 et au-dessus. 
  
Vous pouvez définir la transparence de la couleur du trait dans la cellule LineColorTrans.
  
Pour obtenir une référence à la cellule LineColor par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LineColor  <br/> |
   
Pour obtenir une référence à la cellule LineColor par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLine** <br/> |
|Index de la cellule :  <br/> |**visLineColor** <br/> |
   

