---
title: Cellule YGridSpacing (règle &amp; Section grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1210
localization_priority: Normal
ms.assetid: 30766e13-c90d-62fc-9c98-35ad7b0b4056
description: Précise la distance entre les lignes verticales dans une grille fixe (YGridDensity = 0).
ms.openlocfilehash: 638479719ee0649bf271403249e2cde2ddccf09c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790094"
---
# <a name="ygridspacing-cell-ruler-amp-grid-section"></a>Cellule YGridSpacing (règle &amp; Section grille)

Précise la distance entre les lignes verticales dans une grille fixe (YGridDensity = 0).
  
## <a name="remarks"></a>Remarques

Correspond à l' **Espacement minimal** vertical d’option dans le **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ). 
  
Pour obtenir une référence à la cellule YGridSpacing par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |YGridSpacing  <br/> |
   
Pour obtenir une référence à la cellule YGridSpacing par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowRulerGrid** <br/> |
|Index de la cellule :  <br/> |**visYGridSpacing** <br/> |
   

