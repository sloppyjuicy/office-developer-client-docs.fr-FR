---
title: Élément RefBy (complexType Cell_Type) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Cette énumération spécifie une référence à une page dans le dessin.
ms.openlocfilehash: cb47919a97b8ad42f62bcb1337cd8e6b3596f5ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538311"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>Élément RefBy (complexType Cell_Type) (XML Visio)

Cette énumération spécifie une référence à une page dans le dessin.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |document. xml, Masters. xml, Master #. xml, pages. xml, page #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément de cellule (section balise d’action)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Définit une propriété pour une balise d’action sur une forme ou une page.  <br/> |
|[Élément de cellule (ligne Actions)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété d’une action associée à une commande personnalisée dans un menu contextuel ou de balise d’action.  <br/> |
|[Élément de cellule (ligne ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la coordonnée x, la coordonnée y ou la courbure d’un arc circulaire.  <br/> |
|[Élément de cellule (section caractères)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme pour la séquence de texte d’une forme, comme la police, la couleur, le style, la casse, la position par rapport à la ligne de base ou la taille du point.  <br/> |
|[Élément de cellule (ligne Connection)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, le sens horizontal ou vertical, ou le type d’un point de connexion unique sur une forme.  <br/> |
|[Élément de cellule (ligne Controls)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient une propriété pour une poignée de contrôle spécifique définie pour une forme.  <br/> |
|[Élément de cellule (ligne Ellipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du centre de l’ellipse et de deux points sur l’ellipse.  <br/> |
|[Élément de cellule (ligne EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’un arc elliptique, les coordonnées x ou y des points de contrôle de l’arc, l’angle entre l’axe x et l’axe principal de l’ellipse, ou le rapport entre les axes principal et secondaire de l’ellipse.  <br/> |
|[Élément de cellule (section champ)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ.  <br/> |
|[Élément de cellule (section remplissage dégradé)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la couleur, la transparence et la position d’un point de dégradé pour un dégradé de remplissage.  <br/> |
|[Élément de cellule (section géométrie)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Définit les propriétés qui déterminent la mise en forme et les propriétés comportementales relatives aux lignes et aux arcs qui composent la section Geometry.  <br/> |
|[Élément de cellule (ligne Hyperlink)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les informations d'un seul lien hypertexte associé à une forme. Une forme contient une ligne Hyperlink pour chaque lien hypertexte.  <br/> |
|[Élément de cellule (ligne InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y de deux points sur une ligne infinie.  <br/> |
|[Élément de cellule (section calque)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété pour une couche ou ses propriétés pour une page.  <br/> |
|[Élément de cellule (section dégradé de lignes)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la couleur, la transparence ou la position d’un point de dégradé pour un dégradé de ligne.  <br/> |
|[Élément de cellule (ligne LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du sommet de fin d’un segment de ligne droite.  <br/> |
|[Élément de cellule (ligne MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du premier sommet d’une forme, ou représente les coordonnées x ou y du premier sommet après une cassure d’un chemin d’accès.  <br/> |
|[Élément de cellule (ligne NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, la position de l’avant-dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur ou la formule pour une courbe B-spline rationnelle inuniforme (NURBS).  <br/> |
|[Élément de cellule (section paragraphe)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme de paragraphe pour le texte de la forme, comme les retraits, l’interligne, les puces ou l’alignement horizontal des paragraphes.  <br/> |
|[Élément de cellule (ligne PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du dernier point d’une polyligne ou une formule de polyligne.  <br/> |
|[Élément de cellule (ligne RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de fin d’une courbe de Bézier cubique par rapport à la largeur et la hauteur de la forme, les coordonnées x ou y du point de contrôle du début de la largeur et de la hauteur de la forme relative de la courbe, ou les coordonnées x ou y du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de courbe.  <br/> |
|[Élément de cellule (ligne RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y d’un point de terminaison d’arc elliptique par rapport à la largeur et la hauteur de la forme, les coordonnées x ou y des points de contrôle de l’arc par rapport à la largeur et la hauteur de la forme, l’angle entre l’axe x et l’axe principal de l’ellipse, ou le rapport entre le axes principaux et secondaires de l’ellipse.  <br/> |
|[Élément de cellule (ligne RelLineTo)](cell-element-rellineto-rowvisio-xml.md) [Cellule](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du sommet de fin d’un segment de ligne droite en fonction de la largeur et de la hauteur d’une forme.  <br/> |
|[Élément de cellule (ligne RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du premier sommet d’une forme, ou les coordonnées x ou y du premier sommet après la rupture d’un chemin, par rapport à la hauteur et à la largeur de la forme.  <br/> |
|[Élément de cellule (section RelQuadBezTo](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de fin d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme ou les coordonnées x ou y du point de contrôle de la largeur et de la hauteur de la forme relative de la courbe.  <br/> |
|[Élément de cellule (section Scratch)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une zone de travail permettant d’entrer et de tester des formules auxquelles d’autres cellules peuvent être désignées.  <br/> |
|[Élément de cellule (section données de forme](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété des données de forme.  <br/> |
|[Élément de cellule (ligne SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient des coordonnées x ou y pour le point de contrôle d’une spline ou le nœud d’une spline.  <br/> |
|[Élément de cellule (section SplineStart](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient des coordonnées x ou y pour le deuxième point de contrôle d’une spline, son deuxième nœud, son premier nœud, le dernier nœud ou le degré de la spline.  <br/> |
|[Élément de cellule (section onglets)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété qui contrôle la position ou l’alignement du taquet de tabulation de style et de forme.  <br/> |
|[Élément de cellule (section cellules définies par l’utilisateur)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Une propriété d’une information spécifiée par l’utilisateur qui peut être référencée par d’autres cellules et outils complémentaires.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’ID d’une page dans le dessin.  <br/> |Valeurs du type xsd: unsignedInt.  <br/> |
|T  <br/> |xsd: String  <br/> |obligatoire  <br/> |Spécifie le type de référence.  <br/> |Valeurs du type xsd: String.  <br/> |
   

