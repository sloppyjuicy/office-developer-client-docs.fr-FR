---
title: ShdwScaleFactor, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Indique le pourcentage d'agrandissement ou de réduction de la forme d'une ombre.
ms.openlocfilehash: 99bc48f5332830512e1f5c2f6d93c70b67197c03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789704"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>ShdwScaleFactor, cellule (section Page Properties)

Indique le pourcentage d'agrandissement ou de réduction de la forme d'une ombre. 
  
## <a name="remarks"></a>Remarques

Chaque ombre a un axe d’ombre, qui est un point sur l’ombre qui correspond à l’axe de la forme. Par exemple, si le code confidentiel d’une forme est au centre de la forme, alors l’emplacement de l’axe est le point central de l’ombre. Lors de l’application à l’échelle à des ombres simples, l’agrandissement est centré à l’emplacement de l’axe ; lors de l’application à l’échelle à des ombres obliques, facteur d’agrandissement est appliqué dans la direction oblique. 
  
 Ce pourcentage est utilisé lorsque le type d’ombre d’une forme est défini sur Page Default (la cellule ShapeShdwType est ** visFSTPageDefault **). 
  
Pour définir ce comportement pour une forme individuelle, utilisez la cellule ShapeShdwScaleFactor dans la section Fill Format.
  
Cette valeur correspond à la valeur dans la zone **facteur d’agrandissement** de l’onglet **ombres** de la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ). 
  
Pour obtenir une référence à la cellule ShdwScaleFactor par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ShdwScaleFactor  <br/> |
   
Pour obtenir une référence à la cellule ShdwScaleFactor par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageShdwScaleFactor** <br/> |
   

