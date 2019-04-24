---
title: Cellule YRulerDensity (section &amp; règle et grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1215
localization_priority: Normal
ms.assetid: aebcd321-9d1c-e04e-7c85-3ec1ed851561
description: Définit les graduations verticales de la règle pour la page.
ms.openlocfilehash: c92c48f6c86fc794cf6f53a87fdb99e67a73b9f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357203"
---
# <a name="yrulerdensity-cell-ruler-amp-grid-section"></a>Cellule YRulerDensity (section &amp; règle et grille)

Définit les graduations verticales de la règle pour la page.
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
|0  <br/> |Fixed  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Grossier  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (valeur par défaut)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Précisément  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l'option sous- **divisions** verticales de la boîte de dialogue **grille de &amp; règle** (sous l'onglet **affichage** , cliquez sur la flèche **Afficher** ). 
  
Pour obtenir une référence à la cellule YRulerDensity par un nom dans une autre formule ou dans un programme en faisant appel à la propriété**CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |YRulerDensity  <br/> |
   
Pour obtenir une référence à la cellule YRulerDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowRulerGrid** <br/> |
|Index de la cellule :  <br/> |**visYRulerDensity** <br/> |
   

