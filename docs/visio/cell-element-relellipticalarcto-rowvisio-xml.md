---
title: Élément de cellule (ligne RelEllipticalArcTo) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: beaa8860-807e-c8dd-8a59-29cd0f91ba45
description: Contient les coordonnées x ou y du point de terminaison d’un arc elliptique par rapport à la largeur et à la hauteur de la forme, les coordonnées x ou y des points de contrôle sur l’arc par rapport à la largeur et à la hauteur de la forme, l’angle entre l’axe des x et l’axe principal de l’ellipse, ou le rapport entre les axes principal et mineur de l’ellipse.
ms.openlocfilehash: 6e71b5f3eb8201cfa6bfd7b9f529fab4d2558585
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613085"
---
# <a name="cell-element-relellipticalarcto-row-visio-xml"></a>Élément de cellule (ligne RelEllipticalArcTo) (Visio XML)

Contient les coordonnées x ou y du point de terminaison d’un arc elliptique par rapport à la largeur et à la hauteur de la forme, les coordonnées x ou y des points de contrôle sur l’arc par rapport à la largeur et à la hauteur de la forme, l’angle entre l’axe des x et l’axe principal de l’ellipse, ou le rapport entre les axes principal et mineur de l’ellipse.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Élément Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelEllipticalArcTo_Type](relellipticalarcto_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’un arc elliptique par rapport à la largeur et à la hauteur de la forme, les coordonnées x ou y des points de contrôle sur l’arc par rapport à la largeur et à la hauteur de la forme, l’angle entre l’axe des x et l’axe principal de l’ellipse, ou le rapport entre les axes principal et mineur de l’ellipse.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page de dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |facultatif  <br/> |Indique que la formule est évaluée à une erreur. La valeur de **E** est la valeur actuelle (chaîne de message d’erreur) ; la valeur de **l’attribut V** est la dernière valeur valide.  <br/> |Chaîne de message d’erreur.  <br/> |
|F  <br/> |xsd:string  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir l’une des chaînes suivantes :  <br/>  '(une formule)' si la formule existe localement  <br/>  `No Formula` si la formule est supprimée ou bloquée localement  <br/>  `Inh` si la formule est héritée.  <br/> |Formule.  <br/> |
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet.  <br/> |Nom de la cellule ShapeSheet.  <br/> Voir la section Remarques ci-dessous.  <br/> |
|U  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente une unité de mesure La valeur par défaut est DL.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |Valeur de la cellule ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Remarques

**L’attribut N** de cet **élément Cell** doit faire partie d’un ensemble limité de valeurs qui correspondent aux cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet **élément Cell.** 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|X  <br/> |Coordonnée x du sommet de fin sur un arc par rapport à la largeur de la forme.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|O  <br/> |Coordonnée y du sommet de fin sur un arc par rapport à la hauteur de la forme.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |Coordonnée x du point de contrôle de l’arc par rapport à la largeur de la forme ; point sur l’arc.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |Coordonnée y du point de contrôle d’un arc par rapport à la largeur de la forme.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |Angle de l’axe principal d’un arc par rapport à l’axe X de son parent.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |Rapport entre l’axe principal d’un arc et son axe mineur.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
   

