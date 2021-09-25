---
title: Row, élément (Geometry Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.
ms.openlocfilehash: cf04e8fad2ccccc135b70d530799cc93f2c42fb3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573445"
---
# <a name="row-element-geometry-section-visio-xml"></a>Row, élément (Geometry Section) (Visio XML)

Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

> [!NOTE]
> L’élément Cell est le seul enfant de cet élément. Selon l’attribut « T » de cet élément, la signification des éléments Cell diffère. Dans le tableau ci-dessous, le texte parathetique dans le nom de l’élément correspond à la valeur « T » à laquelle la rubrique s’applique. 
  
|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Élément de cellule (ligne ArcTo)](arcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y et la courbure d'un arc circulaire.  <br/> |
|[Élément de cellule (ligne Ellipse)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du centre et de deux points de l'ellipse.  <br/> |
|[Élément de cellule (ligne EllipticalArcTo)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y d'une extrémité d'arc elliptique, les coordonnées x et y des points de contrôle de l'arc, l'angle entre l'axe x et le grand axe de l'ellipse ainsi que le rapport entre les grand et petit axes de cette dernière.  <br/> |
|[Élément de cellule (ligne InfiniteLine)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y de deux points sur une ligne infinie.  <br/> |
|[Élément de cellule (ligne LineTo)](lineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du dernier sommet d'un segment de droite.  <br/> |
|[Élément de cellule (ligne MoveTo)](moveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du premier sommet d'une forme ou représente les coordonnées x et y du premier sommet après une rupture de chemin.  <br/> |
|[Élément de cellule (ligne NURBSTo)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y, la position de l'avant-dernier nœud, de la dernière épaisseur, du premier nœud, de la première épaisseur et la formule d'une courbe B-spline rationnelle non uniforme (NURBS).  <br/> |
|[Élément de cellule (ligne PolyLineTo)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du dernier point d'une polyligne et une formule de polyligne.  <br/> |
|[Élément de cellule (ligne RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y du point de contrôle du début de la largeur et de la hauteur de la forme relative de courbe, ainsi que les coordonnées x et y du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe.  <br/> |
|[Élément de cellule (ligne RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme et aux coordonnées x et y du point de contrôle de la largeur et de la hauteur de la forme relative de courbe.  <br/> |
|[Élément de cellule (ligne RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de terminaison d’un arc elliptique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y des points de contrôle sur l’arc par rapport à la largeur et à la hauteur de la forme, l’angle entre l’axe des x et l’axe principal de l’ellipse et les proportions entre les axes principal et mineur de l’ellipse.  <br/> |
|[Élément de cellule (ligne RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du sommet de fin d’un segment de trait droit par rapport à la largeur et à la hauteur d’une forme.  <br/> |
|[Élément de cellule (ligne RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du premier sommet d’une forme ou les coordonnées x et y du premier sommet après un rupture dans un chemin d’accès, par rapport à la hauteur et à la largeur de la forme.  <br/> |
|[Élément de cellule (ligne RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme et aux coordonnées x et y du point de contrôle de la largeur et de la hauteur de la forme relative de courbe.  <br/> |
|[Élément de cellule (ligne SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de contrôle et du nœud d'une spline.  <br/> |
|[Élément de cellule (ligne SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y d'un deuxième point de contrôle de spline, du deuxième nœud, du premier nœud, du dernier nœud et du degré de la spline.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si une ligne qui aurait été héritée d’une forme de maître a été supprimée.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’identificateur à base un de la ligne. Il doit être non unique et supérieur aux autres identificateurs de la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs. Une ligne ne peut avoir qu’un des attributs IX ou N.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom unique dépendant de la langue de la ligne.  <br/> |Valeurs du type xsd:string.  <br/> |
|N  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom unique indépendant de la langue de la ligne. L’attribut N est utilisé uniquement pour les sections User, Property, Actions, Control, Connection, Hyperlink et ActionTag. Une ligne ne peut avoir qu’un des attributs IX ou N.  <br/> |Valeurs du type xsd:string.  <br/> |
|T  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation de géométrie. L’attribut T est utilisé uniquement pour la section Geometry.  <br/> |Valeurs du type xsd:string.  <br/> |
   
## <a name="remarks"></a>Remarques

**L’attribut T** de cet **élément Row** doit faire partie d’un ensemble limité de valeurs qui correspondent aux lignes ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **T** qui sont autorisées pour cet **élément Row.** 
  
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
|RelCubBezTo  <br/> |Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y du point de contrôle du début de la largeur et de la hauteur de la forme relative de courbe, ainsi que les coordonnées x et y du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Contient les coordonnées x et y du point de terminaison d’un arc elliptique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y des points de contrôle sur l’arc par rapport à la largeur et à la hauteur de la forme, l’angle entre l’axe des x et l’axe principal de l’ellipse et les proportions entre les axes principal et mineur de l’ellipse.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Contient les coordonnées x et y du sommet de fin d’un segment de trait droit par rapport à la largeur et à la hauteur d’une forme.  <br/> |[RelLineTo Row (Geometry Section)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Contient les coordonnées x et y du premier sommet d’une forme ou les coordonnées x et y du premier sommet après un rupture dans un chemin d’accès, par rapport à la hauteur et à la largeur de la forme.  <br/> |[RelMoveTo Row (Geometry Section)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme et aux coordonnées x et y du point de contrôle de la largeur et de la hauteur de la forme relative de courbe.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Contient les coordonnées x et y du point de contrôle et du nœud d'une spline.  <br/> |[SplineKnot, ligne (section Geometry)](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Contient les coordonnées x et y d'un deuxième point de contrôle de spline, du deuxième nœud, du premier nœud, du dernier nœud et du degré de la spline.  <br/> |[SplineStart, ligne (section Geometry)](splinestart-row-geometry-section.md) <br/> |
   

