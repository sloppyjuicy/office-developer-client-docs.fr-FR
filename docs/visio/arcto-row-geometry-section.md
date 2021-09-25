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
ms.openlocfilehash: 28cf822d71021d7fe4264dd6b4269974e3a75bb6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603913"
---
# <a name="arcto-row-geometry-section"></a>ArcTo Row (Geometry Section)

Contient les  *coordonnées x*  - et  *y*  - et courbe d’un arc circulaire. 
  
La ligne ArcTo contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordonnée  *x*  du sommet de fin d’un arc.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordonnée  *y*  du sommet de fin d’un arc.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Distance entre le milieu de l'arc et le milieu de sa corde.  <br/> |
   
## <a name="remarks"></a>Remarques

Les arcs dessinés dans Visio sont des arcs elliptiques, même s'ils sont basés sur des cercles. Par défaut, les arcs dessinés sont représentés par une ligne EllipticalArcTo dans la fenêtre Feuille ShapeSheet. Pour afficher une ligne ArcTo dans une fenêtre Feuille ShapeSheet, vous devez dessiner un arc puis changer le type de ligne EllipticalArcTo en type de ligne ArcTo ; de ce fait, vous changez un arc elliptique en arc circulaire.
  
Pour changer de type de ligne, cliquez avec le bouton droit de la souris sur la ligne, puis cliquez sur **Modifier le type de ligne** dans le menu contextuel. 
  

