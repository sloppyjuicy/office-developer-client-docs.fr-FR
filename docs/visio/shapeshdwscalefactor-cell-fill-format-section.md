---
title: ShapeShdwScaleFactor, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Indique le pourcentage d'agrandissement ou de réduction possible de l'ombre d'une forme.
ms.openlocfilehash: 0b6392030e7efc8ea36c8d728b99c9b82482840b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789684"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>ShapeShdwScaleFactor, cellule (section Fill Format)

Indique le pourcentage d'agrandissement ou de réduction possible de l'ombre d'une forme.
  
## <a name="remarks"></a>Remarques

Chaque ombre a un axe d’ombre, qui est un point sur l’ombre qui correspond à l’axe de la forme. Par exemple, si le code confidentiel d’une forme est au centre de la forme, alors l’emplacement de l’axe est le point central de l’ombre. Lors de l’application à l’échelle à des ombres simples, l’agrandissement est centré à l’emplacement de l’axe ; lors de l’application à l’échelle à des ombres obliques, facteur d’agrandissement est appliqué dans la direction oblique. 
  
Pour définir cette valeur pour toutes les formes d'une page, utilisez la cellule ShdwScaleFactor de la section Page Properties.
  
Cette valeur correspond à la valeur du paramètre **facteur d’agrandissement** de la boîte de dialogue **ombre** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **ombre**, puis cliquez sur **Options d’ombres**).
  
Pour obtenir une référence à la cellule ShapeShdwScaleFactor par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ShapeShdwScaleFactor  <br/> |
   
Pour obtenir une référence à la cellule ShapeShdwScaleFactor par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillShdwScaleFactor** <br/> |
   

