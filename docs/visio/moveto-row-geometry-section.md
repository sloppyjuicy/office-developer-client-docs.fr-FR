---
title: MoveTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
ms.localizationpriority: medium
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Contient les coordonnées x et y du premier sommet d’une forme, ou représente les coordonnées x et y du premier sommet après une coupure dans un chemin d’accès.
ms.openlocfilehash: 65c01e823ce2f936205139f38380cc4f250e92fe
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62788856"
---
# <a name="moveto-row-geometry-section"></a>MoveTo, ligne (section Geometry)

Contient les  *coordonnées x*  et  *y*  du premier sommet d’une forme, ou représente les coordonnées  *x*  et  *y*  du premier sommet après une coupure dans un chemin d’accès. 
  
Une **ligne MoveTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Si la **ligne MoveTo** est la première ligne de la section, la cellule X représente la coordonnée  *x*  du premier sommet d’une forme. Si la **ligne MoveTo** apparaît entre deux lignes, la cellule X représente la coordonnée  *x*  du premier vertex après la rupture du chemin d’accès. |
|[Y](y-cell-geometry-section.md) <br/> |Si la **ligne MoveTo** est la première ligne de la section, la cellule Y représente la coordonnée  *y*  du premier sommet d’une forme. Si la **ligne MoveTo** apparaît entre deux lignes, la cellule Y représente la coordonnée  *y*  du premier sommet après la coupure du chemin d’accès. |
   
## <a name="remarks"></a>Remarques

La **ligne MoveTo** contient les  *coordonnées x*  et  *y*  du premier sommet de la forme si la **ligne MoveTo** est la première ligne de la section. Il s’agit généralement du premier sommet placé lorsque la forme a été dessinée et il ne correspond pas nécessairement au point de début d’une forme 1D. 
  
Une section Geometry doit commencer par une ligne **RelMoveTo** ou **MoveTo** , mais vous pouvez également utiliser les lignes **MoveTo** et **RelMoveTo** pour représenter un espace dans le tracé du chemin d’une forme. Cependant, lorsque le chemin est utilisé pour définir la limite d'une zone remplie, cet espace est interprété comme un  segment de trait droit. Pour insérer un tel intervalle, insérez une ligne entre deux lignes et modifiez le type de ligne **en MoveTo**. Si la **ligne MoveTo** se trouve entre deux lignes, elle contient les coordonnées  *x*  et  *y*  du premier sommet de la ligne après la rupture du chemin d’accès de la forme. 
  

