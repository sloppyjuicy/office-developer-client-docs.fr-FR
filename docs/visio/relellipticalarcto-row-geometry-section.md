---
title: RelEllipticalArcTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Contient les coordonnées x et y du point de terminaison d’un arc elliptique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y des points de contrôle sur l’arc par rapport à la largeur et à la hauteur de la forme, l’angle entre l’axe x et l’axe principal de l’ellipse, ainsi que les proportions entre les axes principal et mineur de l’ellipse.
ms.openlocfilehash: bba227750895928a2ab4103cd2193d16222813e6
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370531"
---
# <a name="relellipticalarcto-row-geometry-section"></a>RelEllipticalArcTo Row (Geometry Section)

Contient les coordonnées *x* et *y* du point de terminaison d’un arc elliptique par rapport à la largeur et à la hauteur de la forme, les coordonnées *x* et *y* des points de contrôle sur l’arc par rapport à la largeur et à la hauteur de la forme, l’angle entre l’axe *x* et l’axe principal de l’ellipse, ainsi que les proportions entre les axes principal et mineur de l’ellipse.
  
> [!NOTE]
> Une **ligne RelEllipticalArcTo** ne peut être persistante que dans les formats de fichier .vsdx, .vsdm, .vstx, .vstm, .vssx et .vssm. Lorsqu’un fichier est enregistré dans les formats Visio 2003-2010, la ligne **RelEllipticalArcTo** est convertie en ligne [EllipticalArcTo](ellipticalarcto-row-geometry-section.md).
  
Une **ligne RelEllipticalArcTo contient** les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x* du sommet de fin sur un arc par rapport à la largeur de la forme. |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y* du sommet de fin sur un arc par rapport à la hauteur de la forme. |
|[A](a-cell-geometry-section.md) <br/> |Coordonnée *x* du point de contrôle de l’arc par rapport à la largeur de la forme ; point sur l’arc. Le point de contrôle est mieux situé à mi-chemin entre les vertex de début et de fin de l’arc. Dans le cas contraire, l’arc peut atteindre une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles. |
|[B](b-cell-geometry-section.md) <br/> |Coordonnée *y* du point de contrôle d’un arc par rapport à la largeur de la forme. |
|[C](c-cell-geometry-section.md) <br/> |Angle de l’axe principal d’un arc par rapport à *l’axe x* de son parent. |
|[D](d-cell-geometry-section.md) <br/> |Rapport entre l'axe majeur de l'arc et son axe mineur. Contrairement à la signification réelle de ces termes, l'axe « majeur » ne doit pas forcément être plus grand que l'axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles. |

## <a name="remarks"></a>Remarques

Les valeurs de la **ligne RelEllipticalArcTo** sont équivalentes aux valeurs d’une ligne [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) , multipliées par la largeur et la hauteur de la forme. Par exemple : une ligne **RelEllipticalArcTo** où les cellules **X**, **Y**, **A**, **B**, **C** et **D** ont les valeurs 1, 1, 1.5, 0.5, 15 deg et 1.5 (respectivement) peuvent être remplacées par une ligne **EllipticalArcTo** avec les formules `Width*1``Height*1'`de cellule , `Width*1.5`, , , `Height*0.5`15 deg et 1,5 (respectivement).
  