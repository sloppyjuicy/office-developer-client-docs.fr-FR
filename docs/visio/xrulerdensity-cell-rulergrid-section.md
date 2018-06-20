---
title: Cellule XRulerDensity (règle &amp; Section grille)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Définit les graduations horizontales de la règle pour la page.
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790059"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a>Cellule XRulerDensity (règle &amp; Section grille)

Définit les graduations horizontales de la règle pour la page.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
|0  <br/> |Fixe  <br/> |**visRulerFixed** <br/> |
|8 (&amp;H8)  <br/> |Épais  <br/> |**visRulerCoarse** <br/> |
|16 (&amp;H10)  <br/> |Normal (valeur par défaut)  <br/> |**visRulerNormal** <br/> |
|32 (&amp;H20)  <br/> |Fin  <br/> |**visRulerFine** <br/> |
   
## <a name="remarks"></a>Remarques

Cette cellule correspond à l’option **graduations** horizontale de la **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ). 
  
Pour obtenir une référence à la cellule XRulerDensity par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |XRulerDensity  <br/> |
   
Pour obtenir une référence à la cellule XRulerDensity par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowRulerGrid** <br/> |
|Index de la cellule :  <br/> |**visXRulerDensity** <br/> |
   

