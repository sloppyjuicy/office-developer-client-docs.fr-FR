---
title: Cellule YGridDensity (section &amp; règle et grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Indique le type de grille verticale à utiliser.
ms.openlocfilehash: 793fa40316edd591c8b4873d8919507c2393b5d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307706"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Cellule YGridDensity (section &amp; règle et grille)

Indique le type de grille verticale à utiliser.
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visGridFixed** <br/> |
|n°2  <br/> |Grossier  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (valeur par défaut)  <br/> |**visGridNormal** <br/> |
|8bits  <br/> |Précisément  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l'option espacement de la **grille** verticale dans la boîte de dialogue **grille de &amp; règle** (sous l'onglet **affichage** , cliquez sur la flèche **Afficher** ). 
  
Pour obtenir une référence à la cellule XGridDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |YGridDensity  <br/> |
   
Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowRulerGrid** <br/> |
|Index de la cellule :  <br/> |**visYGridDensity** <br/> |
   

