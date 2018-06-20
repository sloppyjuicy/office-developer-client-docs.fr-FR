---
title: RelMoveTo, ligne (Section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Contient x - et y - coordonnées du premier sommet d’une forme ou x - et y-coordonnées du premier sommet après une rupture de chemin, par rapport à la hauteur et la largeur de la forme.
ms.openlocfilehash: 77b3e731bfd1f35abe34ffbf3155b57133e56412
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789444"
---
# <a name="relmoveto-row-geometry-section"></a>RelMoveTo, ligne (Section Geometry)

Contient *x* - et *y* - coordonnées du premier sommet d’une forme ou *x* - et *y* -coordonnées du premier sommet après une rupture de chemin, par rapport à la hauteur et la largeur de la forme. 
  
> [!NOTE]
> Une ligne **RelMoveTo** peut uniquement être conservée dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats de Visio 2003 à 2010, la ligne **RelMoveTo** est convertie en une ligne [MoveTo](moveto-row-geometry-section.md) . 
  
Une ligne **RelMoveTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Si la ligne **RelMoveTo** est la première ligne dans la section, la cellule X représente la *x* -coordonnées du premier sommet d’une forme par rapport à la largeur de la forme. Si la ligne **RelMoveTo** apparaît entre deux lignes, la cellule X représente la *x* -coordonnées du premier sommet après la rupture du chemin d’accès.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Si la ligne **RelMoveTo** est la première ligne dans la section, la cellule Y représente la valeur *y* -coordonnées du premier sommet d’une forme. Si la ligne **RelMoveTo** apparaît entre deux lignes, la cellule Y représente la valeur *y* -coordonnées du premier sommet après la rupture du chemin d’accès.  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs dans la ligne **RelMoveTo** sont équivalents aux valeurs d’une ligne [MoveTo](moveto-row-geometry-section.md) sont multipliées par la largeur et la hauteur de la forme. Par exemple : une ligne **RelMoveTo** où la valeur de la cellule **X** est « 0 » et la valeur de la cellule **Y** est « 0,5 » pourrait être remplacée par la ligne **MoveTo** où la valeur de la cellule **X** est la formule « largeur*0" et la cellule **Y** est le formule « hauteur*0,5. » 
  
La ligne **RelMoveTo** contient les coordonnées *x* - et *y* -coordonnées du premier sommet de la forme si la ligne MoveTo est la première ligne dans la section. Généralement, il s’agit du premier sommet placé lors de la forme a été dessinée, et il ne correspond pas nécessairement au point de début d’une forme 1D. 
  
Une section **Geometry** doit commencer par un **MoveTo** ou une ligne **RelMoveTo** , mais vous pouvez également utiliser la ligne de **RelMoveTo** et de la ligne **MoveTo** pour représenter un espace dans le traçage du chemin d’accès d’une forme par rapport à la largeur et la hauteur de la forme. Toutefois, lorsque le chemin d’accès est utilisée pour définir la limite d’une zone remplie, cet intervalle est interprétée comme un segment de trait droit. Pour insérer un espace, insérer une ligne entre deux lignes et changez le type de ligne **RelMoveTo**. Si la ligne **RelMoveTo** est entre deux lignes, elle contient les coordonnées *x* - et *y* -coordonnées du premier sommet de la ligne après la rupture de chemin d’accès de la forme. 
  

