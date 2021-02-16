---
title: XGridDensity, cellule (section Ruler &amp; Grid)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Indique le type de grille horizontale à utiliser.
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436040"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>XGridDensity, cellule (section Ruler &amp; Grid)

Indique le type de grille horizontale à utiliser.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visGridFixed** <br/> |
|2   <br/> |Entâyé  <br/> |**visGridCoarse** <br/> |
|4   <br/> |Normal (valeur par défaut)  <br/> |**visGridNormal** <br/> |
|8   <br/> |Fine  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l’option  espacement grille horizontal dans  la boîte de dialogue Grille de règle (sous l’onglet Affichage, cliquez sur **Afficher** la flèche). **&amp;** 
  
Pour obtenir une référence à la cellule XGridDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |XGridDensity  <br/> |
   
Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowRulerGrid** <br/> |
|Index de la cellule :  <br/> |**visXGridDensity** <br/> |
   

