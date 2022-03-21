---
title: YRulerDensity, cellule (section Ruler &amp; Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
ms.localizationpriority: medium
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Définit les graduations verticales de la règle pour la page.
ms.openlocfilehash: 46247e19f83ff5131fecf162ccf2104fb54c24a1
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630955"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>YRulerDensity, cellule (section Ruler &amp; Grid)

Définit les graduations verticales de la règle pour la page.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Entâyé  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (valeur par défaut)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Fine  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l’option **Subdivisions verticales** dans la boîte de dialogue **Grille &amp;** de règles  (sous l’onglet Affichage, cliquez sur **Afficher** la flèche). 
  
Pour obtenir une référence à la cellule YRulerDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |YRulerDensity  <br/> |
   
Pour obtenir une référence à la cellule YRulerDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowRulerGrid** <br/> |
|**Index de la cellule :**  <br/> |**visYRulerDensity** <br/> |
   

