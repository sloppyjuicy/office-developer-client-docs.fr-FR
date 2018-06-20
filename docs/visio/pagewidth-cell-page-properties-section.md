---
title: PageWidth, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Détermine la largeur de la page imprimée en unités de dessin.
ms.openlocfilehash: e03696c8f1c921c930d3563e9c73ef4ae613a7c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789225"
---
# <a name="pagewidth-cell-page-properties-section"></a>PageWidth, cellule (section Page Properties)

Détermine la largeur de la page imprimée en unités de dessin.
  
## <a name="remarks"></a>Remarques

Vous pouvez également définir la largeur de la page sous l’onglet **Taille de la Page** de la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ) ou redimensionnez manuellement la page avec la souris. Pour ce faire, faites glisser la bordure de la page tout en maintenant la touche CTRL enfoncée. 
  
Pour obtenir une référence à la cellule PageWidth par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |PageWidth  <br/> |
   
Pour obtenir une référence à la cellule PageWidth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPage** <br/> |
|Index de la cellule :  <br/> |**visPageWidth** <br/> |
   

