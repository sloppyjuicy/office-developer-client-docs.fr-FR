---
title: XRulerDensity, cellule (section Ruler &amp; Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
ms.localizationpriority: medium
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Définit les graduations horizontales de la règle pour la page.
ms.openlocfilehash: 23eacc8e1a99df92bf9cdb705adda6cb3ecad890
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603108"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>XRulerDensity, cellule (section Ruler &amp; Grid)

Définit les graduations horizontales de la règle pour la page.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visRulerFixed** <br/> |
|8 ( &amp; H8)  <br/> |Entâyé  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (valeur par défaut)  <br/> |**visRulerNormal** <br/> |
|32 ( &amp; H20)  <br/> |Fine  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l’option **Subdivisions** horizontale dans  la boîte de dialogue **Grille &amp;** de règles (sous l’onglet Affichage, cliquez sur **Afficher** la flèche). 
  
Pour obtenir une référence à la cellule XRulerDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |XRulerDensity  <br/> |
   
Pour obtenir une référence à la cellule XRulerDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowRulerGrid** <br/> |
|Index de la cellule :  <br/> |**visXRulerDensity** <br/> |
   

