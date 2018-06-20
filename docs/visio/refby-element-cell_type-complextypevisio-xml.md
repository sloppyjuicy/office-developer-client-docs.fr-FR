---
title: Élément RefBy (Cell_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Spécifie une référence à une page dans le dessin.
ms.openlocfilehash: 4d3f131ba5fc106c886d30d8561e095972b05a21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789400"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>Élément RefBy (Cell_Type, complexType) (« Visio XML »)

Spécifie une référence à une page dans le dessin.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.XML, masters.xml, maître # .xml, pages.xml, page # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément de cellule (Section balises d’Action)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Définit une propriété pour une balise d’action sur une forme ou une page.  <br/> |
|[Élément de cellule (ligne Actions)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété d’une action associée à une commande personnalisée dans un menu contextuel ou action de la balise.  <br/> |
|[Élément de cellule (ligne ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient le x coordonnée, coordonnée y ou courbure d’un arc circulaire.  <br/> |
|[Élément de cellule (Section Character)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme de la séquence de texte d’une forme, comme la police, la couleur, de style, cas, la position relative à la ligne de base ou taille en points.  <br/> |
|[Élément de cellule (ligne de connexion)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, sens horizontal ou vertical ou le type d’un point de connexion unique d’une forme.  <br/> |
|[Élément de cellule (ligne)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient une propriété d’une poignée de contrôle définie pour une forme.  <br/> |
|[Élément de cellule (ligne Ellipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du centre et de deux points sur l’ellipse.  <br/> |
|[Élément de cellule (ligne EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’un arc elliptique coordonnées x ou y du contrôle pointe sur l’arc, l’angle de l’axe x à l’axe majeur de l’ellipse ou rapport entre axes principaux et secondaires de l’ellipse.  <br/> |
|[Élément de cellule (Section champs)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue champ.  <br/> |
|[Élément de cellule (Section dégradé remplissage)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la couleur, la transparence et la position d’un point de dégradé pour un dégradé de remplissage.  <br/> |
|[Élément de cellule (Section Geometry)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Définit les propriétés qui déterminent les propriétés de mise en forme et le comportement en ce qui concerne les traits et des arcs qui constituent la Section Geometry.  <br/> |
|[Élément de cellule (ligne lien hypertexte)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les informations d'un seul lien hypertexte associé à une forme. Une forme contient une ligne Hyperlink pour chaque lien hypertexte.  <br/> |
|[Élément de cellule (ligne InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y de deux points sur une ligne infinie.  <br/> |
|[Élément de cellule (Section Layer)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété d’un calque ou ses propriétés pour une page.  <br/> |
|[Élément de cellule (Section dégradé ligne)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la couleur, la transparence ou la position d’un point de dégradé pour un dégradé de ligne.  <br/> |
|[Élément de cellule (ligne LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient x- ou la coordonnée y du sommet de fin d’un segment de trait droit.  <br/> |
|[Élément de cellule (ligne MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du premier sommet d’une forme ou représente les coordonnées x ou y du premier sommet après une rupture de chemin.  <br/> |
|[Élément de cellule (ligne NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la position x ou y coordonnées, du deuxième au dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur ou la formule d’une courbe B-spline rationnelle (NURBS).  <br/> |
|[Élément de cellule (Section Paragraph)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie un attribut pour le texte de la forme, telles que les retraits, l’espacement des lignes, des puces ou alignement horizontal des paragraphes de la mise en forme de paragraphe.  <br/> |
|[Élément de cellule (ligne PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du dernier point d’une polyligne ou une formule de polyligne.  <br/> |
|[Élément de cellule (RelCubBezTo ligne)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y de l’extrémité d’une courbe de Bézier cube par rapport à la hauteur et la largeur de la forme, les coordonnées x ou y du point de contrôle de début de la hauteur et la largeur de la courbe relative d’une forme ou les coordonnées x ou y du point de contrôle de la fin de la largeur et la hauteur de la forme relative courbe.  <br/> |
|[Élément de cellule (RelEllipticalArcTo ligne)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’un arc par rapport à la largeur et la hauteur de la forme coordonnées x ou y du contrôle pointe sur l’arc par rapport à la forme width et height, angle à partir de l’axe des x à l’axe majeur de l’ellipse ou rapport entre la axes principaux et secondaires de l’ellipse.  <br/> |
|[Élément de cellule (RelLineTo ligne)](cell-element-rellineto-rowvisio-xml.md) [Cellule](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient x- ou la coordonnée y du sommet de fin d’un segment de droite par rapport à la largeur et la hauteur d’une forme.  <br/> |
|[Élément de cellule (RelMoveTo ligne)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du premier sommet d’une forme ou les coordonnées x ou y du premier sommet après une rupture de chemin, par rapport à la hauteur et la largeur de la forme.  <br/> |
|[Élément de cellule (RelQuadBezTo Section](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’une courbe de Bézier par rapport à la hauteur et la largeur de la forme ou les coordonnées x ou y du point de contrôle de la largeur et la hauteur de la forme relative courbe.  <br/> |
|[Élément de cellule (Section Scratch)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie un espace de travail pour entrer et tester des formules qui peuvent être appelés à d’autres cellules.  <br/> |
|[Élément de cellule (Section Shape Data](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété de données de forme.  <br/> |
|[Élément de cellule (ligne SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de contrôle ou le nœud d’une spline.  <br/> |
|[Élément de cellule (SplineStart Section](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y pour le deuxième point de contrôle d’une spline, du deuxième nœud, du premier nœud, du dernier nœud ou le degré de la spline.  <br/> |
|[Élément de cellule (Section Tabs)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété qui contrôle la position du taquet shape et style ou l’alignement.  <br/> |
|[Élément de cellule (Section de cellules définies par l’utilisateur)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Une propriété d’un élément spécifié par l’utilisateur des informations susceptibles d’être référencées par d’autres cellules et outils de module complémentaire.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’ID d’une page dans le dessin.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|T  <br/> |XSD : String  <br/> |obligatoire  <br/> |Spécifie le type de référence.  <br/> |Valeurs du type xsd : String.  <br/> |
   

