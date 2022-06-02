---
title: Élément Row (section Geometry) (Visio XML)
description: L’élément Row (Section Geometry) (Visio XML) contient des lignes qui répertorient les coordonnées des sommets pour les lignes et les arcs qui composent la forme.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
ms.openlocfilehash: 33a6370f9576fee551684c08eba9877b055ba480
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853117"
---
# <a name="row-element-geometry-section-visio-xml"></a>Élément Row (section Geometry) (Visio XML)

Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **la séquence**, **minOccurs**, **maxOccurs** et **le choix**, consultez la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contient les lignes qui répertorient les coordonnées des sommets des traits et des arcs qui constituent la forme. |
   
### <a name="child-elements"></a>Éléments enfants

> [!NOTE]
> L’élément Cell est le seul enfant de cet élément. Selon l’attribut « T » de cet élément, la signification des éléments Cell diffère. Dans le tableau ci-dessous, le texte parathétique dans le nom de l’élément correspond à la valeur « T » à laquelle la rubrique s’applique. 
  
|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Élément de cellule (ligne ArcTo)](arcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y et la courbure d'un arc circulaire. |
|[Élément de cellule (ligne Ellipse)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du centre et de deux points de l'ellipse. |
|[Élément de cellule (ligne EllipticalArcTo)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y d'une extrémité d'arc elliptique, les coordonnées x et y des points de contrôle de l'arc, l'angle entre l'axe x et le grand axe de l'ellipse ainsi que le rapport entre les grand et petit axes de cette dernière. |
|[Élément de cellule (ligne InfiniteLine)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y de deux points sur une ligne infinie. |
|[Élément de cellule (ligne LineTo)](lineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du dernier sommet d'un segment de droite. |
|[Élément de cellule (ligne MoveTo)](moveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du premier sommet d'une forme ou représente les coordonnées x et y du premier sommet après une rupture de chemin. |
|[Élément de cellule (ligne NURBSTo)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y, la position de l'avant-dernier nœud, de la dernière épaisseur, du premier nœud, de la première épaisseur et la formule d'une courbe B-spline rationnelle non uniforme (NURBS). |
|[Élément de cellule (ligne PolyLineTo)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du dernier point d'une polyligne et une formule de polyligne. |
|[Élément de cellule (ligne RelCubBezTo)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de terminaison d’une courbe bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y du point de contrôle du début de la largeur et de la hauteur de la forme relative de la courbe, ainsi que les coordonnées x et y du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de la courbe. |
|[Élément de cellule (ligne RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme et aux coordonnées x et y du point de contrôle de la largeur et de la hauteur de la forme relative de la courbe. |
|[Élément de cellule (ligne RelEllipticalArcTo)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de terminaison d’un arc elliptique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y des points de contrôle sur l’arc par rapport à la largeur et à la hauteur de la forme, l’angle de l’axe X à l’axe principal de l’ellipse et le rapport entre les axes principaux et mineurs de l’ellipse. |
|[Élément de cellule (ligne RelLineTo)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du sommet de fin d’un segment de ligne droite par rapport à la largeur et à la hauteur d’une forme. |
|[Élément de cellule (ligne RelMoveTo)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du premier sommet d’une forme ou les coordonnées x et y du premier vertex après un saut dans un chemin, par rapport à la hauteur et à la largeur de la forme. |
|[Élément de cellule (ligne RelQuadBezTo)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme et aux coordonnées x et y du point de contrôle de la largeur et de la hauteur de la forme relative de la courbe. |
|[Élément de cellule (ligne SplineKnot)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y du point de contrôle et du nœud d'une spline. |
|[Élément de cellule (ligne SplineStart)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Contient les coordonnées x et y d'un deuxième point de contrôle de spline, du deuxième nœud, du premier nœud, du dernier nœud et du degré de la spline. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Spécifie si une ligne qui serait autrement héritée d’une forme principale a été supprimée. |Valeurs du type xsd:boolean. |
|IX  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |Spécifie l’identificateur à base unique pour la ligne. Il doit être unqiue et supérieur à d’autres identificateurs dans la même section. L’attribut IX est utilisé uniquement pour les sections Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch et Tabs. Une ligne ne peut avoir qu’un seul des attributs IX ou N. |Valeurs du type xsd:unsignedInt. |
|LocalName  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom unique dépendant de la langue de la ligne. |Valeurs du type xsd:string. |
|N  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le nom unique indépendant du langage de la ligne. L’attribut N est utilisé uniquement pour les sections Utilisateur, Propriété, Actions, Contrôle, Connexion, Lien hypertexte et ActionTag. Une ligne ne peut avoir qu’un seul des attributs IX ou N. |Valeurs du type xsd:string. |
|T  <br/> |xsd:string  <br/> |facultatif  <br/> |Spécifie le type du chemin géométrique représenté par la ligne et utilisé dans la visualisation géométrique. L’attribut T est utilisé uniquement pour la section Geometry. |Valeurs du type xsd:string. |
   
## <a name="remarks"></a>Remarques

L’attribut **T** de cet élément **Row** doit être l’un des ensembles limités de valeurs qui correspondent aux lignes ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **T** autorisées pour cet élément **Row** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Contient les coordonnées x et y et la courbure d'un arc circulaire. |[ArcTo, ligne (section Geometry)](arcto-row-geometry-section.md) <br/> |
|Ellipse  <br/> |Contient les coordonnées x et y du centre et de deux points de l'ellipse. |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Contient les coordonnées x et y d'une extrémité d'arc elliptique, les coordonnées x et y des points de contrôle de l'arc, l'angle entre l'axe x et le grand axe de l'ellipse ainsi que le rapport entre les grand et petit axes de cette dernière. |[EllipticalArcTo, ligne (section Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Contient les coordonnées x et y de deux points sur une ligne infinie. |[InfiniteLine, ligne (section Geometry)](infiniteline-row-geometry-section.md) |
|Lineto  <br/> |Contient les coordonnées x et y du dernier sommet d'un segment de droite. |[LineTo, ligne (section Geometry)](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Contient les coordonnées x et y du premier sommet d'une forme ou représente les coordonnées x et y du premier sommet après une rupture de chemin. |[MoveTo, ligne (section Geometry)](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Contient les coordonnées x et y, la position de l'avant-dernier nœud, de la dernière épaisseur, du premier nœud, de la première épaisseur et la formule d'une courbe B-spline rationnelle non uniforme (NURBS). |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Contient les coordonnées x et y du dernier point d'une polyligne et une formule de polyligne. |[PolylineTo, ligne (section Geometry)](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Contient les coordonnées x et y du point de terminaison d’une courbe bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y du point de contrôle du début de la largeur et de la hauteur de la forme relative de la courbe, ainsi que les coordonnées x et y du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de la courbe. |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Contient les coordonnées x et y du point de terminaison d’un arc elliptique par rapport à la largeur et à la hauteur de la forme, les coordonnées x et y des points de contrôle sur l’arc par rapport à la largeur et à la hauteur de la forme, l’angle de l’axe X à l’axe principal de l’ellipse et le rapport entre les axes principaux et mineurs de l’ellipse. |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Contient les coordonnées x et y du sommet de fin d’un segment de ligne droite par rapport à la largeur et à la hauteur d’une forme. |[RelLineTo Row (Geometry Section)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Contient les coordonnées x et y du premier sommet d’une forme ou les coordonnées x et y du premier vertex après un saut dans un chemin, par rapport à la hauteur et à la largeur de la forme. |[RelMoveTo Row (Geometry Section)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Contient les coordonnées x et y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme et aux coordonnées x et y du point de contrôle de la largeur et de la hauteur de la forme relative de la courbe. |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Contient les coordonnées x et y du point de contrôle et du nœud d'une spline. |[SplineKnot, ligne (section Geometry)](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Contient les coordonnées x et y d'un deuxième point de contrôle de spline, du deuxième nœud, du premier nœud, du dernier nœud et du degré de la spline. |[SplineStart, ligne (section Geometry)](splinestart-row-geometry-section.md) <br/> |
   

