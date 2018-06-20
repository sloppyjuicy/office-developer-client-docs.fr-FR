---
title: MoveTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Contient les coordonnées x - et y - les coordonnées du premier sommet d’une forme ou représente le x - et y-coordonnées du premier sommet après une rupture de chemin d’accès.
ms.openlocfilehash: cee62701074269350ae52c6fa7f7aee5cb612f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789155"
---
# <a name="moveto-row-geometry-section"></a>MoveTo, ligne (section Geometry)

Contient les coordonnées *x* - et *y* - les coordonnées du premier sommet d’une forme ou représente le *x* - et *y* -coordonnées du premier sommet après une rupture de chemin d’accès. 
  
Une ligne **MoveTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Si la ligne **MoveTo** est la première ligne dans la section, la cellule X représente la *x* -coordonnées du premier sommet d’une forme. Si la ligne **MoveTo** apparaît entre deux lignes, la cellule X représente la *x* -coordonnées du premier sommet après la rupture du chemin d’accès.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Si la ligne **MoveTo** est la première ligne dans la section, la cellule Y représente la valeur *y* -coordonnées du premier sommet d’une forme. Si la ligne **MoveTo** apparaît entre deux lignes, la cellule Y représente la valeur *y* -coordonnées du premier sommet après la rupture du chemin d’accès.  <br/> |
   
## <a name="remarks"></a>Remarques

La ligne **MoveTo** contient les coordonnées *x* - et *y* -coordonnées du premier sommet de la forme si la ligne **MoveTo** est la première ligne dans la section. Généralement, il s’agit du premier sommet placé lors de la forme a été dessinée, et il ne correspond pas nécessairement au point de début d’une forme 1D. 
  
Une section geometry doit commencer par un **RelMoveTo** ou une ligne **MoveTo** , mais vous pouvez également utiliser les lignes **MoveTo** et **RelMoveTo** pour représenter un espace dans le traçage du chemin d’accès d’une forme. Toutefois, lorsque le chemin d’accès est utilisée pour définir la limite d’une zone remplie, cet intervalle est interprétée comme un segment de trait droit. Pour insérer un espace, insérer une ligne entre deux lignes et changez le type de ligne **MoveTo**. Si la ligne **MoveTo** est entre deux lignes, elle contient les coordonnées *x* - et *y* -coordonnées du premier sommet de la ligne après la rupture de chemin d’accès de la forme. 
  

