---
title: Cellule XGridDensity (règle &amp; Section grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Indique le type de grille verticale à utiliser.
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790093"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Cellule XGridDensity (règle &amp; Section grille)

Indique le type de grille verticale à utiliser.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Fixe  <br/> |**visGridFixed** <br/> |
|2  <br/> |Épais  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (valeur par défaut)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Fin  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l' **espacement** vertical d’option dans le **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ). 
  
Pour obtenir une référence à la cellule XGridDensity par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |XGridDensity  <br/> |
   
Pour obtenir une référence à la cellule XGridDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowRulerGrid** <br/> |
|Index de la cellule :  <br/> |**visYGridDensity** <br/> |
   

