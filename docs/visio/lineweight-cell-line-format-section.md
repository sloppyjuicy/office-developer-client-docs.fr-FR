---
title: LineWeight, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
ms.localizationpriority: medium
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Détermine l’épaisseur d’un trait. Pour définir l’épaisseur, entrez un nombre accompagné d’une unité de mesure valide.
ms.openlocfilehash: 48a34ff02c01fa76d7cc13c6bbef597d89ca7d3a
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63507795"
---
# <a name="lineweight-cell-line-format-section"></a>LineWeight, cellule (section Line Format)

Détermine l’épaisseur d’un trait. Pour définir l’épaisseur, entrez un nombre accompagné d’une unité de mesure valide.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de LineWeight dans la boîte de dialogue **Trait** (sous l’onglet **Trait**, dans le groupe **Forme**, cliquez sur **Trait**, pointez sur **Épaisseur**, puis cliquez sur **Autres traits**).
  
Si l’unité de mesure n’est pas entrée, l’unité de mesure du texte spécifié dans la boîte de dialogue **Options Visio** est utilisée (cliquez  sur l’onglet Fichier, puis sur **Options**). L’épaisseur de trait est indépendante de l’échelle du dessin. Si le dessin est mis à l’échelle, l’épaisseur de trait ne change pas. 
  
Pour obtenir une référence à la cellule LineWeight par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | LineWeight  <br/> |
   
Pour obtenir une référence à la cellule LineWeight à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowLine** <br/> |
| **Index de la cellule :**  <br/> |**visLineWeight** <br/> |
   

