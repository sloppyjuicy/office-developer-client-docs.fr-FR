---
title: PageWidth, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
ms.localizationpriority: medium
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Détermine la largeur de la page imprimée en unités de dessin.
ms.openlocfilehash: 6e791216757b41e7f3e38704ede372b0c519c201
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521875"
---
# <a name="pagewidth-cell-page-properties-section"></a>PageWidth, cellule (section Page Properties)

Détermine la largeur de la page imprimée en unités de dessin.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la largeur de page sous  l’onglet Taille de  page de la boîte de dialogue Mise  en page (sous l’onglet Création, cliquez sur la flèche Mise en **page**) ou en re dimensionner manuellement la page avec la souris. Pour ce faire, faites glisser le bord de la page en maintenant la touche Ctrl enfoncée. 
  
Pour obtenir une référence à la cellule PageWidth par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |PageWidth  <br/> |
   
Pour obtenir une référence à la cellule PageWidth à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowPage** <br/> |
|**Index de la cellule :**  <br/> |**visPageWidth** <br/> |
   

