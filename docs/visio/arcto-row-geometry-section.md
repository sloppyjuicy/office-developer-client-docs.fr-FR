---
title: ArcTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
ms.localizationpriority: medium
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Contient les coordonnées x - et y - et courbe d’un arc circulaire.
ms.openlocfilehash: 096da7d57f1579f1bcf3b4c9ae950c9c85d1cfe8
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783690"
---
# <a name="arcto-row-geometry-section"></a>ArcTo Row (Geometry Section)

Contient les  *coordonnées x*  - et  *y*  - et courbe d’un arc circulaire. 
  
La ligne ArcTo contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée *x*  du sommet de fin d’un arc. |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée *y*  du sommet de fin d’un arc. |
|[A](a-cell-geometry-section.md) <br/> |Distance entre le milieu de l'arc et le milieu de sa corde. |
   
## <a name="remarks"></a>Remarques

Les arcs dessinés dans Visio sont des arcs elliptiques, même s'ils sont basés sur des cercles. Par défaut, les arcs dessinés sont représentés par une ligne EllipticalArcTo dans la fenêtre Feuille ShapeSheet. Pour afficher une ligne ArcTo dans une fenêtre Feuille ShapeSheet, vous devez dessiner un arc puis changer le type de ligne EllipticalArcTo en type de ligne ArcTo ; de ce fait, vous changez un arc elliptique en arc circulaire.
  
Pour changer de type de ligne, cliquez avec le bouton droit de la souris sur la ligne, puis cliquez sur **Modifier le type de ligne** dans le menu contextuel. 
  

