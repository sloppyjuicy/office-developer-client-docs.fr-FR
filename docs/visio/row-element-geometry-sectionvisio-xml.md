---
title: Élément de ligne (Section Geometry) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: Contient des lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.
ms.openlocfilehash: 1581c87ae34eff4f01054a2340c18f1e55456cfb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581691"
---
# <a name="row-element-geometry-section-visio-xml"></a>Élément de ligne (Section Geometry) (« Visio XML »)

Contient des lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |master # .xml, page # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contient des lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

> [!NOTE]
> L’élément de cellule est le seul enfant de cet élément. En fonction de l’attribut « T » de cet élément, la signification d’éléments de la cellule diffèrent. Dans le tableau ci-dessous, texte parathetical dans le nom de l’élément correspond à la valeur « T » à laquelle s’applique la rubrique. 
  
|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément de cellule (ligne ArcTo)](arcto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y et la courbure d'un arc circulaire.  <br/> |
|[Élément de cellule (ligne Ellipse)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du centre et de deux points de l'ellipse.  <br/> |
|[Élément de cellule (ligne EllipticalArcTo)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y d'une extrémité d'arc elliptique, les coordonnées x et y des points de contrôle de l'arc, l'angle entre l'axe x et le grand axe de l'ellipse ainsi que le rapport entre les grand et petit axes de cette dernière.  <br/> |
|[Élément de cellule (ligne InfiniteLine)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y de deux points sur une ligne infinie.  <br/> |
|[Élément de cellule (ligne LineTo)](lineto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du dernier sommet d'un segment de droite.  <br/> |
|[Élément de cellule (ligne MoveTo)](moveto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du premier sommet d'une forme ou représente les coordonnées x et y du premier sommet après une rupture de chemin.  <br/> |
|[Élément de cellule (ligne NURBSTo)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y, la position de l'avant-dernier nœud, de la dernière épaisseur, du premier nœud, de la première épaisseur et la formule d'une courbe B-spline rationnelle non uniforme (NURBS).  <br/> |
|[Élément de cellule (ligne PolyLineTo)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du dernier point d'une polyligne et une formule de polyligne.  <br/> |
|[Élément de cellule (ligne RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y de l’extrémité d’une courbe de Bézier cube par rapport à la hauteur et la largeur de la forme, les coordonnées x et y du point de contrôle de début de la hauteur et la largeur de la courbe relative d’une forme et les coordonnées x et y du contrôle point de fin de la largeur et la hauteur de la forme relative courbe.  <br/> |
|[Élément de cellule (ligne RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y de l’extrémité d’une courbe de Bézier par rapport à la hauteur et la largeur de la forme et les coordonnées x et y du point de contrôle de la largeur et la hauteur de la forme relative courbe.  <br/> |
|[Élément de cellule (ligne RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de terminaison d’un arc par rapport à la hauteur et la largeur de la forme, les coordonnées x et y de l’arc par rapport à la largeur de la forme et height, angle à partir de l’axe des x à l’axe majeur de l’ellipse ainsi que le rapport entre les points de contrôle axes principaux et secondaires de l’ellipse.  <br/> |
|[Élément de cellule (ligne RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient x- et la coordonnée y du sommet de fin d’un segment de droite par rapport à la largeur et la hauteur d’une forme.  <br/> |
|[Élément de cellule (ligne RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du premier sommet d’une forme ou les coordonnées x et y du premier sommet après une rupture de chemin, par rapport à la hauteur et la largeur de la forme.  <br/> |
|[Élément de cellule (ligne RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y de l’extrémité d’une courbe de Bézier par rapport à la hauteur et la largeur de la forme et les coordonnées x et y du point de contrôle de la largeur et la hauteur de la forme relative courbe.  <br/> |
|[Élément de cellule (ligne SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de contrôle et du nœud d'une spline.  <br/> |
|[Élément de cellule (ligne SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](http://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y d'un deuxième point de contrôle de spline, du deuxième nœud, du premier nœud, du dernier nœud et du degré de la spline.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|SUPPR.  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Spécifie si une ligne qui sinon serait héritée à partir d’une forme de base a été supprimée.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’identificateur de base 1 pour la ligne. Il doit être unique et supérieur à d’autres identificateurs dans la même section. L’attribut IX est utilisée uniquement pour les caractère, connexion, champ, FillGradient, sections Geometry, Layer, LineGradient, paragraphe, réviseur, zéro et onglets. Une ligne peut être un des attributs IX ou N.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|LocalName  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le nom unique dépendant de la langue de la ligne.  <br/> |Valeurs du type xsd : String.  <br/> |
|N  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le nom indépendant du langage unique de la ligne. L’attribut N est utilisée uniquement pour les sections utilisateur, propriété, Actions, contrôle, connexion, lien hypertexte et ActionTag. Une ligne peut être un des attributs IX ou N.  <br/> |Valeurs du type xsd : String.  <br/> |
|T  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le type de chemin d’accès géométrique représentée par la ligne et utilisé dans la visualisation de géométrie. L’attribut T est utilisée uniquement pour la section Geometry.  <br/> |Valeurs du type xsd : String.  <br/> |
   
## <a name="remarks"></a>Remarques

L’attribut **T** de **cet élément** doit être un ensemble limité de valeurs qui correspondent aux lignes de feuille ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs autorisées pour cet élément de **ligne** de l’attribut **T** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Contient les coordonnées x et y et la courbure d'un arc circulaire.  <br/> |[ArcTo, ligne (section Geometry)](arcto-row-geometry-section.md) <br/> |
|Ellipse  <br/> |Contient les coordonnées x et y du centre et de deux points de l'ellipse.  <br/> |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Contient les coordonnées x et y d'une extrémité d'arc elliptique, les coordonnées x et y des points de contrôle de l'arc, l'angle entre l'axe x et le grand axe de l'ellipse ainsi que le rapport entre les grand et petit axes de cette dernière.  <br/> |[EllipticalArcTo, ligne (section Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Contient les coordonnées x et y de deux points sur une ligne infinie.  <br/> |[InfiniteLine, ligne (section Geometry)](infiniteline-row-geometry-section.md) |
|LineTo  <br/> |Contient les coordonnées x et y du dernier sommet d'un segment de droite.  <br/> |[LineTo, ligne (section Geometry)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Contient les coordonnées x et y du premier sommet d'une forme ou représente les coordonnées x et y du premier sommet après une rupture de chemin.  <br/> |[MoveTo, ligne (section Geometry)](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Contient les coordonnées x et y, la position de l'avant-dernier nœud, de la dernière épaisseur, du premier nœud, de la première épaisseur et la formule d'une courbe B-spline rationnelle non uniforme (NURBS).  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Contient les coordonnées x et y du dernier point d'une polyligne et une formule de polyligne.  <br/> |[PolylineTo, ligne (section Geometry)](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Contient les coordonnées x et y de l’extrémité d’une courbe de Bézier cube par rapport à la hauteur et la largeur de la forme, les coordonnées x et y du point de contrôle de début de la hauteur et la largeur de la courbe relative d’une forme et les coordonnées x et y du contrôle point de fin de la largeur et la hauteur de la forme relative courbe.  <br/> |[Ligne RelCubBezTo (section Géométrie)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Contient les coordonnées x et y du point de terminaison d’un arc par rapport à la hauteur et la largeur de la forme, les coordonnées x et y de l’arc par rapport à la largeur de la forme et height, angle à partir de l’axe des x à l’axe majeur de l’ellipse ainsi que le rapport entre les points de contrôle axes principaux et secondaires de l’ellipse.  <br/> |[Ligne RelEllipticalArcTo (section Géométrie)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Contient x- et la coordonnée y du sommet de fin d’un segment de droite par rapport à la largeur et la hauteur d’une forme.  <br/> |[Ligne RelLineTo (section Géométrie)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Contient les coordonnées x et y du premier sommet d’une forme ou les coordonnées x et y du premier sommet après une rupture de chemin, par rapport à la hauteur et la largeur de la forme.  <br/> |[Ligne RelMoveTo (section Géométrie)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Contient les coordonnées x et y de l’extrémité d’une courbe de Bézier par rapport à la hauteur et la largeur de la forme et les coordonnées x et y du point de contrôle de la largeur et la hauteur de la forme relative courbe.  <br/> |[Ligne RelQuadBezTo (section Géométrie)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Contient les coordonnées x et y du point de contrôle et du nœud d'une spline.  <br/> |[SplineKnot, ligne (section Geometry)](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Contient les coordonnées x et y d'un deuxième point de contrôle de spline, du deuxième nœud, du premier nœud, du dernier nœud et du degré de la spline.  <br/> |[SplineStart, ligne (section Geometry)](splinestart-row-geometry-section.md) <br/> |
   

