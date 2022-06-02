---
title: RefBy, élément (Cell_Type complexType) (Visio XML)
description: Décrit la description et les informations d’élément parent/enfant pour l’élément RefBy (Cell_Type complexType), qui spécifie une référence à une page dans le dessin.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
ms.openlocfilehash: 5ea49a0094c2044db16217288a599ae858b26173
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853082"
---
# <a name="refby-element-cell_type-complextype-visio-xml"></a>RefBy, élément (Cell_Type complexType) (Visio XML)

Spécifie une référence à une page dans le dessin.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **la séquence**, **minOccurs**, **maxOccurs** et **le choix**, consultez la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Élément Cell (section Action Tag)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Définit une propriété pour une balise d’action sur une forme ou une page. |
|[Élément de cellule (ligne Actions)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété d’une action associée à une commande personnalisée dans un menu contextuel ou de balise d’action. |
|[Élément de cellule (ligne ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la coordonnée x, la coordonnée y ou l’arc d’un arc circulaire. |
|[Élément Cell (section Character)](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme pour l’exécution de texte d’une forme, tel que la police, la couleur, le style, la casse, la position par rapport à la ligne de base ou la taille du point. |
|[Élément de cellule (ligne Connection)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, la direction horizontale ou verticale, ou le type d’un point de connexion unique sur une forme. |
|[Élément de cellule (ligne Controls)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient une propriété pour un handle de contrôle particulier défini pour une forme. |
|[Élément de cellule (ligne Ellipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point central de l’ellipse et deux points sur l’ellipse. |
|[Élément de cellule (ligne EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’un arc elliptique, les coordonnées x ou y des points de contrôle sur l’arc, l’angle de l’axe X à l’axe principal de l’ellipse, ou le rapport entre les axes majeurs et mineurs de l’ellipse. |
|[Élément Cell (section Field)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Affiche les fonctions et formules insérées dans le texte de la forme à l’aide de la boîte de dialogue Champ. |
|[Élément Cell (Fill Gradient Section)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la couleur, la transparence et la position d’un point de dégradé pour un dégradé de remplissage. |
|[Élément Cell (section Geometry)](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Définit les propriétés qui déterminent la mise en forme et les propriétés comportementales par rapport aux lignes et aux arcs qui composent la section Geometry. |
|[Élément de cellule (ligne Hyperlink)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les informations d'un seul lien hypertexte associé à une forme. Une forme contient une ligne Hyperlink pour chaque lien hypertexte. |
|[Élément de cellule (ligne InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y de deux points sur une ligne infinie. |
|[Élément Cell (section Layer)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété pour une couche ou ses propriétés pour une page. |
|[Élément Cell (Line Gradient Section)](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient la couleur, la transparence ou la position d’un point de dégradé pour un dégradé de ligne. |
|[Élément de cellule (ligne LineTo)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du sommet de fin d’un segment de ligne droite. |
|[Élément de cellule (ligne MoveTo)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du premier sommet d’une forme, ou représente les coordonnées x ou y du premier vertex après un saut dans un chemin d’accès. |
|[Élément de cellule (ligne NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, la position de l’avant-dernier nœud, la position du dernier poids, la position du premier nœud, la position du premier poids ou la formule d’un B-spline rationnel non uniforme (NURBS). |
|[Élément Cell (Section Paragraph)](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie un attribut de mise en forme de paragraphe pour le texte de la forme, tel que les retraits, l’espacement des lignes, les puces ou l’alignement horizontal des paragraphes. |
|[Élément de cellule (ligne PolyLineTo)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient des coordonnées x ou y du dernier point d’une polyligne ou d’une formule polyligne. |
|[Élément de cellule (ligne RelCubBezTo)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’une courbe bézier cubique par rapport à la largeur et à la hauteur de la forme, les coordonnées x ou y du point de contrôle du début de la largeur et de la hauteur de la forme relative de la courbe, ou les coordonnées x ou y du point de contrôle de la fin de la largeur et de la hauteur de la forme relative de la courbe. |
|[Élément de cellule (ligne RelEllipticalArcTo)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’un arc elliptique par rapport à la largeur et à la hauteur de la forme, les coordonnées x ou y des points de contrôle sur l’arc par rapport à la largeur et à la hauteur de la forme, l’angle de l’axe X à l’axe principal de l’ellipse ou le rapport entre les axes principaux et mineurs de l’ellipse. |
|[Élément cell (RelLineTo Row)](cell-element-rellineto-rowvisio-xml.md)[Cell](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient des coordonnées x ou y du sommet de fin d’un segment de ligne droite par rapport à la largeur et à la hauteur d’une forme. |
|[Élément de cellule (ligne RelMoveTo)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du premier sommet d’une forme, ou les coordonnées x ou y du premier sommet après un saut dans un chemin, par rapport à la hauteur et à la largeur de la forme. |
|[Élément Cell (section RelQuadBezTo)](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme ou aux coordonnées x ou y du point de contrôle de la largeur et de la hauteur de la forme relative de la courbe. |
|[Élément Cell (Scratch Section)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une zone de travail pour entrer et tester des formules qui peuvent être référencées par d’autres cellules. |
|[Élément Cell (section Données de forme](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété des données de forme. |
|[Élément de cellule (ligne SplineKnot)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient des coordonnées x ou y pour le point de contrôle d’un spline ou le nœud d’un spline. |
|[Élément Cell (section SplineStart](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Contient des coordonnées x ou y pour le deuxième point de contrôle d’un spline, son deuxième nœud, son premier nœud, le dernier nœud ou le degré de spline. |
|[Élément Cell (section Tabs)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété qui contrôle la position ou l’alignement des taquets de tabulation de forme et de style. |
|[Élément Cell (section Cellules définies par l’utilisateur)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Propriété d’une information spécifiée par l’utilisateur qui peut être référencée par d’autres cellules et outils de module complémentaire. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |Spécifie l’ID d’une page dans le dessin. |Valeurs du type xsd:unsignedInt. |
|T  <br/> |xsd:string  <br/> |obligatoire  <br/> |Spécifie le type de référence. |Valeurs du type xsd:string. |
   

