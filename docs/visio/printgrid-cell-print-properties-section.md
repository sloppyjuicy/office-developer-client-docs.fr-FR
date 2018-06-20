---
title: PrintGrid, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Indique si la grille sera imprimée lors de l'impression d'une page de document.
ms.openlocfilehash: 76e5b5b4e82c39cbbffbecc710f05a77dbaa6332
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789371"
---
# <a name="printgrid-cell-print-properties-section"></a>PrintGrid, cellule (section Print Properties)

Indique si la grille sera imprimée lors de l'impression d'une page de document.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Affiche la grille lors de l'impression de cette page.  <br/> |
|FALSE  <br/> |N'affiche pas la grille lors de l'impression de cette page (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Cette valeur correspond à la case à cocher **quadrillage** sous l’onglet **Configuration de l’impression** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ). Autre couleur (la version imprimée est grise), la grille imprimée est identique à la grille s’affiche dans la fenêtre de dessin Microsoft Visio. 
  
Vous pouvez choisir s’il faut imprimer la grille sur une base de page par page. Le style de grille peut également être défini sur une base de page par page dans la **règle &amp; grille** boîte de dialogue (sous l’onglet **affichage** , cliquez sur la flèche **Afficher** ) lorsqu’une page est active. 
  
Pour obtenir une référence à la cellule PrintGrid par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PrintGrid  <br/> |
   
Pour obtenir une référence à la cellule PrintGrid par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
|Index de la cellule :  <br/> |**visPrintPropertiesPrintGrid** <br/> |
   

