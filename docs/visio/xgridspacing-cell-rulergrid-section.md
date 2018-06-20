---
title: Cellule XGridSpacing (règle &amp; Section grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1160
localization_priority: Normal
ms.assetid: e07dd983-7588-6317-944c-46da2bb65b31
description: Précise la distance entre les lignes horizontales dans une grille fixe (XGridDensity = 0).
ms.openlocfilehash: 5f461d02dae1574fe2b186b43166ef14d8251df2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790057"
---
# <a name="xgridspacing-cell-ruler-amp-grid-section"></a>Cellule XGridSpacing (règle &amp; Section grille)

Précise la distance entre les lignes horizontales dans une grille fixe (XGridDensity = 0).
  
## <a name="remarks"></a>Remarques

Cette cellule correspond à l' **Espacement minimal** horizontal d’option dans le **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ). 
  
Pour obtenir une référence à la cellule XGridSpacing par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |XGridSpacing  <br/> |
   
Pour obtenir une référence à la cellule XGridSpacing par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowRulerGrid** <br/> |
|Index de la cellule :  <br/> |**visXGridSpacing** <br/> |
   

