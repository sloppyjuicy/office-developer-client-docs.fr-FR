---
title: Cellule XGridDensity (section &amp; règle et grille)
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
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Cellule XGridDensity (section &amp; règle et grille)

Indique le type de grille horizontale à utiliser.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visGridFixed** <br/> |
|n°2  <br/> |Grossier  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (valeur par défaut)  <br/> |**visGridNormal** <br/> |
|8bits  <br/> |Précisément  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l'option espacement horizontal de la **grille** dans la boîte de dialogue **règle de &amp; règle** (sous l'onglet **affichage** , cliquez sur la flèche **Afficher** ). 
  
Pour obtenir une référence à la cellule XGridDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |XGridDensity  <br/> |
   
Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowRulerGrid** <br/> |
|Index de la cellule :  <br/> |**visXGridDensity** <br/> |
   

