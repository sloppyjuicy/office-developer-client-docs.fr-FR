---
title: Cellule YRulerDensity (règle &amp; Section grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Définit les graduations verticales de la règle pour la page.
ms.openlocfilehash: 4b5dcba7a5cb1a588f742b1c2ea6b430cb2af12c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790091"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>Cellule YRulerDensity (règle &amp; Section grille)

Définit les graduations verticales de la règle pour la page.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Fixe  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Épais  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (valeur par défaut)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Fin  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l’option **graduations** verticale de la **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ). 
  
Pour obtenir une référence à la cellule YRulerDensity par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |YRulerDensity  <br/> |
   
Pour obtenir une référence à la cellule YRulerDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowRulerGrid** <br/> |
|Index de la cellule :  <br/> |**visYRulerDensity** <br/> |
   

