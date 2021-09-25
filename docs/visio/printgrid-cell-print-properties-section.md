---
title: PrintGrid, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
ms.localizationpriority: medium
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Indique si la grille sera imprimée lors de l'impression d'une page de document.
ms.openlocfilehash: e290e28920f3ece4f9493b52b223e85dc3888949
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559758"
---
# <a name="printgrid-cell-print-properties-section"></a>PrintGrid, cellule (section Print Properties)

Indique si la grille sera imprimée lors de l'impression d'une page de document.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Affiche la grille lors de l'impression de cette page.  <br/> |
|FALSE  <br/> |N'affiche pas la grille lors de l'impression de cette page (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Cette valeur correspond à la case à cocher **Quadrillage** sous l’onglet **Configuration** de la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur **Mise en page**). Exception faite de la couleur (la version imprimée est grise), la grille imprimée est identique à celle que vous voyez dans la fenêtre de dessin Microsoft Office Visio. 
  
Vous pouvez choisir d’imprimer la grille page par page. Le style de grille peut également être défini page par page dans la  boîte de  dialogue Grille de règle (sous l’onglet Affichage, cliquez sur Afficher la flèche) lorsqu’une page est active. **&amp;** 
  
Pour obtenir une référence à la cellule PrintGrid par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PrintGrid  <br/> |
   
Pour obtenir une référence à la cellule PrintGrid à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
|Index de la cellule :  <br/> |**visPrintPropertiesPrintGrid** <br/> |
   

