---
title: RelMoveTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Contient les coordonnées x et y du premier sommet d’une forme ou les coordonnées x et y du premier sommet après un rupture de chemin d’accès, par rapport à la hauteur et à la largeur de la forme.
ms.openlocfilehash: 488945dbeeea177514770da57b5f26ac947053a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414199"
---
# <a name="relmoveto-row-geometry-section"></a>RelMoveTo Row (Geometry Section)

Contient les coordonnées  *x*  et  *y*  du premier sommet d’une forme ou les coordonnées  *x*  et  *y*  du premier sommet après un rupture de chemin d’accès, par rapport à la hauteur et à la largeur de la forme. 
  
> [!NOTE]
> Une **ligne RelMoveTo** ne peut être persistante que dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats Visio 2003-2010, la ligne **RelMoveTo** est convertie en ligne [MoveTo.](moveto-row-geometry-section.md) 
  
Une **ligne RelMoveTo** contient les cellules suivantes. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Si la **ligne RelMoveTo** est la première ligne de la section, la cellule X représente la coordonnée  *x*  du premier sommet d’une forme par rapport à la largeur de la forme. Si la **ligne RelMoveTo** apparaît entre deux lignes, la cellule X représente la coordonnée  *x*  du premier sommet après la coupure du chemin d’accès.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Si la **ligne RelMoveTo** est la première ligne de la section, la cellule Y représente la coordonnée  *y*  du premier sommet d’une forme. Si la **ligne RelMoveTo** apparaît entre deux lignes, la cellule Y représente la coordonnée  *y*  du premier sommet après la coupure du chemin d’accès.  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs de **la ligne RelMoveTo** sont équivalentes aux valeurs d’une [ligne MoveTo](moveto-row-geometry-section.md) multipliées par la largeur et la hauteur de la forme. Par exemple : une ligne **RelMoveTo** où la valeur de la cellule **X** est « 0 » et la valeur de la cellule **Y** est « 0,5 » peut être remplacée par la ligne **MoveTo** où la valeur de la cellule **X** est la formule « Width 0 » et la cellule ***Y*** la formule « Height 0.5 ». 
  
La **ligne RelMoveTo** contient les coordonnées  *x*  et  *y*  du premier sommet de la forme si la ligne MoveTo est la première ligne de la section. Il s’agit généralement du premier sommet placé lorsque la forme a été dessinée et il ne correspond pas nécessairement au point de début d’une forme 1D. 
  
Une section **Geometry** doit commencer par une ligne **MoveTo** ou **RelMoveTo,** mais vous pouvez également utiliser les lignes **RelMoveTo** et **MoveTo** pour représenter un espace dans le tracé du chemin d’une forme par rapport à la largeur et à la hauteur de la forme. Cependant, lorsque le chemin est utilisé pour définir la limite d'une zone remplie, cet espace est interprété comme un  segment de trait droit. Pour insérer un tel intervalle, insérez une ligne entre deux lignes et modifiez le type de ligne **en RelMoveTo**. Si la **ligne RelMoveTo** se trouve entre deux lignes, elle contient les coordonnées  *x*  et  *y*  du premier sommet de la ligne après la rupture du chemin d’accès de la forme. 
  

