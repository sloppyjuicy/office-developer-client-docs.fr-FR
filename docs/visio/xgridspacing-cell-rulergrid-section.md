---
title: XGridSpacing, cellule (section Ruler &amp; Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
ms.localizationpriority: medium
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Précise la distance entre les lignes horizontales dans une grille fixe (XGridDensity = 0).
ms.openlocfilehash: 6056d692f88ecb50d15c498dfc700f1e3c500732
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627842"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a>XGridSpacing, cellule (section Ruler &amp; Grid)

Précise la distance entre les lignes horizontales dans une grille fixe (XGridDensity = 0).
  
## <a name="remarks"></a>Remarques

Cette cellule correspond à l’option **&amp;** d’espacement **minimal** horizontal dans la boîte de dialogue Grille de règle  (sous l’onglet Affichage, cliquez sur **Afficher** la flèche). 
  
Pour obtenir une référence à la cellule XGridSpacing par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |XGridSpacing  <br/> |
   
Pour obtenir une référence à la cellule XGridSpacing par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowRulerGrid** <br/> |
|**Index de la cellule :**  <br/> |**visXGridSpacing** <br/> |
   

