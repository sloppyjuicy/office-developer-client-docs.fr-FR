---
title: Élément RefBy (Cell_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Spécifie une référence à une page du dessin.
ms.openlocfilehash: 1b79a0d61cc1ba2cb8fe1ef24c13ccb30d39f55e
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506851"
---
# <a name="refby-element-cell_type-complextype-visio-xml"></a>Élément RefBy (Cell_Type complexType) (Visio XML)

Spécifie une référence à une page du dessin.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément de cellule (section Action Tag)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Définit une propriété pour une balise d’action sur une forme ou une page. |
|[Élément de cellule (ligne Actions)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété d’une action associée à une commande personnalisée dans un menu de raccourci ou de balise d’action. |
|[Élément de cellule (ligne ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la coordonnée x, la coordonnée y ou la courbe d’un arc circulaire. |
|[Élément de cellule (section Character)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme pour l’écriture de texte d’une forme, tel que la police, la couleur, le style, la case, la position par rapport à la ligne de base ou la taille du point. |
|[Élément de cellule (ligne Connection)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, la direction horizontale ou verticale, ou le type d’un point de connexion unique sur une forme. |
|[Élément de cellule (ligne Controls)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient une propriété pour un handle de contrôle particulier défini pour une forme. |
|[Élément de cellule (ligne Ellipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point central de l’ellipse et deux points sur l’ellipse. |
|[Élément de cellule (ligne EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison, des coordonnées x ou y d’un arc elliptique des points de contrôle sur l’arc, l’angle entre l’axe des x et l’axe principal de l’ellipse, ou le rapport entre les axes principal et mineur de l’ellipse. |
|[Élément de cellule (section Field)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ. |
|[Élément de cellule (section Fill Gradient)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la couleur, la transparence et la position d’un dégradé pour un dégradé de remplissage. |
|[Élément de cellule (section Geometry)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Définit les propriétés qui déterminent la mise en forme et les propriétés comportementales par rapport aux lignes et aux arcs qui font la section Geometry. |
|[Élément de cellule (ligne Hyperlink)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les informations d'un seul lien hypertexte associé à une forme. Une forme contient une ligne Hyperlink pour chaque lien hypertexte. |
|[Élément de cellule (ligne InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y de deux points sur une ligne infinie. |
|[Élément de cellule (section Layer)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété pour un calque ou ses propriétés pour une page. |
|[Élément de cellule (section Line Gradient)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la couleur, la transparence ou la position d’un dégradé pour un dégradé de trait. |
|[Élément de cellule (ligne LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du sommet de fin d’un segment de ligne droite. |
|[Élément de cellule (ligne MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du premier sommet d’une forme, ou représente les coordonnées x ou y du premier sommet après une coupure dans un chemin d’accès. |
|[Élément de cellule (ligne NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, la position du deuxième au dernier nœud, la position du dernier poids, la position du premier nœud, la position de la première pondération ou la formule d’une ligne B-spline rationnelle nonuniforme (NURBS). |
|[Élément de cellule (section Paragraph)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme de paragraphe pour le texte de la forme, tel que les retraits, l’espacement des lignes, les puces ou l’alignement horizontal des paragraphes. |
|[Élément de cellule (ligne PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du dernier point d’une polyligne ou d’une formule polyligne. |
|[Élément de cellule (ligne RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’une courbe de Bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées x ou y du point de contrôle du début de la largeur et de la hauteur de la forme relative de courbe, ou les coordonnées x ou y du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe. |
|[Élément de cellule (ligne RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’un arc elliptique par rapport à la largeur et à la hauteur de la forme, les coordonnées x ou y des points de contrôle sur l’arc par rapport à la largeur et à la hauteur de la forme, l’angle entre l’axe des x et l’axe principal de l’ellipse, ou le rapport entre les axes principal et mineur de l’ellipse. |
|[Élément de cellule (ligne RelLineTo)](cell-element-rellineto-rowvisio-xml.md)[Cellule](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du sommet de fin d’un segment de trait droit par rapport à la largeur et à la hauteur d’une forme. |
|[Élément de cellule (ligne RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du premier sommet d’une forme, ou les coordonnées x ou y du premier sommet après une coupure dans un chemin d’accès, par rapport à la hauteur et à la largeur de la forme. |
|[Élément de cellule (section RelQuadBezTo)](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme ou aux coordonnées x ou y du point de contrôle de la largeur et de la hauteur de la forme relative de courbe. |
|[Élément de cellule (section Scratch)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une zone de travail pour l’entrée et le test de formules qui peuvent être référentes par d’autres cellules. |
|[Élément de cellule (section Shape Data)](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété des données de forme. |
|[Élément de cellule (ligne SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient des coordonnées x ou y pour le point de contrôle d’une spline ou le nœud d’une spline. |
|[Élément de cellule (section SplineStart)](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient des coordonnées x ou y pour le deuxième point de contrôle d’une spline, son deuxième nœud, son premier nœud, le dernier nœud ou le degré de la spline. |
|[Élément de cellule (section Tabs)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété qui contrôle la position ou l’alignement des tabulations de forme et de style. |
|[Élément de cellule (section User-defined Cells)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Propriété d’une information spécifiée par l’utilisateur à qui peuvent faire référence d’autres cellules et outils de module complémentaire. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’ID d’une page dans le dessin. |Valeurs du type xsd:unsignedInt. |
|T  <br/> |xsd:string  <br/> |obligatoire  <br/> |Spécifie le type de référence. |Valeurs du type xsd:string. |
   

