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
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436264"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a>ShapeShdwScaleFactor, cellule (section Fill Format)

Indique le pourcentage d'agrandissement ou de réduction possible de l'ombre d'une forme.
  
## <a name="remarks"></a>Remarques

Chaque ombre a un axe d'ombre portée, qui est un point sur l'ombre qui correspond à l'axe de la forme. Par exemple, si l'axe d'une forme est au centre de cette dernière, l'axe d'ombre portée est le point central de l'ombre. Lors de l'application d'une mise à l'échelle à des ombres simples, le facteur d'agrandissement est centré sur l'emplacement du code confidentiel ombré; lors de l'application d'une mise à l'échelle aux ombres obliques, le facteur d'agrandissement est appliqué dans la direction oblique. 
  
Pour définir cette valeur pour toutes les formes d'une page, utilisez la cellule ShdwScaleFactor de la section Page Properties.
  
Cette valeur correspond à celle du paramètre **Facteur d’orientation** de la boîte de dialogue **Ombre** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Ombre**, puis cliquez sur **Options d’ombres**).
  
Pour obtenir une référence à la cellule ShapeShdwScaleFactor par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ShapeShdwScaleFactor  <br/> |
   
Pour obtenir une référence à la cellule ShapeShdwScaleFactor à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowFill** <br/> |
|Index de la cellule :  <br/> |**visFillShdwScaleFactor** <br/> |
   

