---
title: XGridDensity, cellule (section Ruler &amp; Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
ms.localizationpriority: medium
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Indique le type de grille horizontale à utiliser.
ms.openlocfilehash: 238bd9a9619d2ff73837bfbd331b7e8f06551b5e
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627836"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>XGridDensity, cellule (section Ruler &amp; Grid)

Indique le type de grille horizontale à utiliser.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visGridFixed** <br/> |
|2  <br/> |Entâyé  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (valeur par défaut)  <br/> |**visGridNormal** <br/> |
|8   <br/> |Fine  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule  correspond à l’option  **&amp;** espacement grille horizontal dans la boîte de dialogue Grille de règle (sous l’onglet Affichage, cliquez sur **Afficher** la flèche). 
  
Pour obtenir une référence à la cellule XGridDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |XGridDensity  <br/> |
   
Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowRulerGrid** <br/> |
|**Index de la cellule :**  <br/> |**visXGridDensity** <br/> |
   

