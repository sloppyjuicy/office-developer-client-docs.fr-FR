---
title: PolylineTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: Contient des x et y-coordonnées du dernier point d’une polyligne et une formule de polyligne.
ms.openlocfilehash: 56cecb2eeaa1702461b1096fe468974f2f0b1f52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789257"
---
# <a name="polylineto-row-geometry-section"></a>PolylineTo, ligne (section Geometry)

Contient des *x* et *y* -coordonnées du dernier point d’une polyligne et une formule de polyligne. 
  
Une ligne PolylineTo contient les cellules suivantes.
  
|**Cell**|**Description**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -coordonnées du sommet de fin d’une polyligne.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La valeur *y* -coordonnées du sommet de fin d’une polyligne.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Formule de la polyligne.  <br/> |
   
## <a name="remarks"></a>Notes

Lignes représentés sous la forme d’une ligne Polyline sont équivalentes aux lignes représentés sous la forme d’une séquence de lignes LineTo, mais une ligne Polyline est plus efficace. Vous pouvez modifier une ligne PolylineTo en LineTo afin de pouvoir visualiser facilement la géométrie des formes. Pour ce faire, avec le bouton droit de la ligne PolylineTo, puis cliquez sur **Développer la ligne** dans le menu contextuel. 
  
Pour modifier un type de ligne à une ligne PolylineTo, avec le bouton droit de la ligne, puis cliquez sur **Modifier le Type de ligne** dans le menu contextuel. 
  

