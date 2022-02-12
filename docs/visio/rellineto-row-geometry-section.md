---
title: RelLineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contient les coordonnées x et y du sommet de fin d’un segment de trait droit par rapport à la largeur et à la hauteur d’une forme.
ms.openlocfilehash: 79fa1de3503870f39f8b9f53b35271ed070d7079
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779446"
---
# <a name="rellineto-row-geometry-section"></a>RelLineTo Row (Geometry Section)

Contient  *les coordonnées x*  et  *y*  du sommet de fin d’un segment de trait droit par rapport à la largeur et à la hauteur d’une forme. 
  
> [!NOTE]
> Une **ligne RelLineTo** ne peut être persistante que dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats Visio 2003-2010, la ligne **RelLineTo** est convertie en ligne [LineTo](lineto-row-geometry-section.md). 
  
Une **ligne RelLineTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x*  du sommet de fin d’un segment de trait droit par rapport à la largeur de la forme. |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y*  du sommet de fin d’un segment de trait droit par rapport à la hauteur de la forme. |
   
## <a name="remarks"></a>Remarques

Les valeurs de **la ligne RelLineTo** sont équivalentes aux valeurs d’une ligne [LineTo](lineto-row-geometry-section.md) multipliées par la largeur et la hauteur de la forme. Par exemple : une ligne **RelLineTo** où la valeur de la cellule **X** est « 0 » et la valeur de la cellule **Y** est « 0,5 » peut être remplacée par une ligne **LineTo** où la valeur de la cellule **X** est la formule « Width0 » et la cellule ***Y*** la formule « Height0.5 ». 
  

