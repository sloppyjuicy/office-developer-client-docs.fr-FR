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
ms.openlocfilehash: 4222c90552bcf3cfb1425e75b4b5bf2bfe213cae
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426810"
---
# <a name="linecolor-cell-line-format-section"></a>LineColor, cellule (section Line Format)

Détermine la couleur de trait de la forme.
  
## <a name="remarks"></a>Remarques

Pour définir la couleur de trait, entrez un nombre compris entre 0 et 23. Il s’agit d’un index d’un ensemble de couleurs de trait. Vous pouvez afficher l’ensemble de couleurs de trait dans la boîte de dialogue **Trait** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Trait**, pointez sur **Poids**, puis cliquez sur **Autres traits**). Vous pouvez également définir la valeur de LineColor dans la boîte de dialogue **Trait**. 
  
Pour entrer une couleur personnalisée, utilisez la fonction RVB ou TSL. La valeur d’une couleur personnalisée est sa couleur RVB, et RVB( *r, g, b*), au lieu d’un nombre, s’affiche dans la fenêtre Feuille ShapeSheet. Dans les opérations numériques, les couleurs personnalisées ont des valeurs supérieures ou égales à 24. 
  
Vous pouvez définir la transparence de la couleur du trait dans la cellule LineColorTrans.
  
Pour obtenir une référence à la cellule LineColor par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |LineColor  <br/> |
   
Pour obtenir une référence à la cellule LineColor à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowLine** <br/> |
|**Index de la cellule :**  <br/> |**visLineColor** <br/> |
   

