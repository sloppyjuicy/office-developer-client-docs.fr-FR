---
title: ShapeShdwScaleFactor, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
ms.localizationpriority: medium
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Indique le pourcentage d'agrandissement ou de réduction possible de l'ombre d'une forme.
ms.openlocfilehash: 3c68cb9aa7328078ce8d6c56da5297f98afdc908
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573326"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>ShapeShdwScaleFactor, cellule (section Fill Format)

Indique le pourcentage d'agrandissement ou de réduction possible de l'ombre d'une forme.
  
## <a name="remarks"></a>Remarques

Chaque ombre a un axe d'ombre portée, qui est un point sur l'ombre qui correspond à l'axe de la forme. Par exemple, si l'axe d'une forme est au centre de cette dernière, l'axe d'ombre portée est le point central de l'ombre. Lors de l’application d’une échelle à des ombres simples, le grossissement est centré à l’emplacement de la broche ombrée ; lors de l’application d’une échelle aux ombres obliques, le grossissement est appliqué dans le sens oblique. 
  
Pour définir cette valeur pour toutes les formes d'une page, utilisez la cellule ShdwScaleFactor de la section Page Properties.
  
Cette valeur correspond à celle du paramètre **Facteur d’orientation** de la boîte de dialogue **Ombre** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Ombre**, puis cliquez sur **Options d’ombres**).
  
Pour obtenir une référence à la cellule ShapeShdwScaleFactor par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ShapeShdwScaleFactor  <br/> |
   
Pour obtenir une référence à la cellule ShapeShdwScaleFactor à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillShdwScaleFactor** <br/> |
   

