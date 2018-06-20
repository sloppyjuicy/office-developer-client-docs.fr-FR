---
title: RelLineTo, ligne (Section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contient x - et y-coordonnées du sommet de fin d’un segment de droite par rapport à la largeur et la hauteur d’une forme.
ms.openlocfilehash: 26cb63ac6cc0708be4e5668174022af63391c129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789433"
---
# <a name="rellineto-row-geometry-section"></a>RelLineTo, ligne (Section Geometry)

Contient *x* - et *y* -coordonnées du sommet de fin d’un segment de droite par rapport à la largeur et la hauteur d’une forme. 
  
> [!NOTE]
> Une ligne **RelLineTo** peut uniquement être conservée dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats de Visio 2003 à 2010, la ligne **RelLineTo** est convertie en une ligne [LineTo](lineto-row-geometry-section.md) . 
  
Une ligne **RelLineTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordonnées du sommet de fin d’un segment de droite par rapport à la largeur de la forme.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées du sommet de fin d’un segment de droite par rapport à la hauteur de la forme.  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs dans la ligne **RelLineTo** sont équivalents aux valeurs d’une ligne [LineTo](lineto-row-geometry-section.md) sont multipliées par la largeur et la hauteur de la forme. Par exemple : une ligne **RelLineTo** où la valeur de la cellule **X** est « 0 » et la valeur de la cellule **Y** est « 0,5 » peut être remplacée par ligne **LineTo** où la valeur de la cellule **X** est la formule « largeur*0" et la cellule **Y** est le formule « hauteur*0,5. » 
  

