---
title: Élément de cellule (ligne RelEllipticalArcTo) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beaa8860-807e-c8dd-8a59-29cd0f91ba45
description: Contient les coordonnées x ou y du point de terminaison d’un arc par rapport à la largeur et la hauteur de la forme coordonnées x ou y du contrôle pointe sur l’arc par rapport à la forme width et height, angle à partir de l’axe des x à l’axe majeur de l’ellipse ou rapport entre la axes principaux et secondaires de l’ellipse.
ms.openlocfilehash: 55e7f664aaab34aa079bafe8f11c57e99fd8a935
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383155"
---
# <a name="cell-element-relellipticalarcto-row-visio-xml"></a>Élément de cellule (ligne RelEllipticalArcTo) (« Visio XML »)

Contient les coordonnées x ou y du point de terminaison d’un arc par rapport à la largeur et la hauteur de la forme coordonnées x ou y du contrôle pointe sur l’arc par rapport à la forme width et height, angle à partir de l’axe des x à l’axe majeur de l’ellipse ou rapport entre la axes principaux et secondaires de l’ellipse.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |master # .xml, page # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Row, élément (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelEllipticalArcTo_Type](relellipticalarcto_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’un arc par rapport à la largeur et la hauteur de la forme coordonnées x ou y du contrôle pointe sur l’arc par rapport à la forme width et height, angle à partir de l’axe des x à l’axe majeur de l’ellipse ou rapport entre la axes principaux et secondaires de l’ellipse.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page de dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD : String  <br/> |facultatif  <br/> |Indique que la formule génère une erreur. La valeur de **E** est la valeur actuelle (chaîne message d’erreur) ; la valeur de l’attribut de **V** est la dernière valeur valide.  <br/> |Chaîne de message d’erreur.  <br/> |
|F  <br/> |XSD : String  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir une des chaînes suivantes :  <br/>  « (une formule) » si la formule existe localement  <br/>  `No Formula`Si la formule est localement supprimée ou bloquée  <br/>  `Inh`Si la formule est héritée.  <br/> |Une formule.  <br/> |
|N  <br/> |XSD : String  <br/> |obligatoire  <br/> |Représente le nom de la cellule de feuille ShapeSheet.  <br/> |Le nom de la cellule de feuille ShapeSheet.  <br/> Voir la section Remarques ci-dessous.  <br/> |
|U  <br/> |XSD : String  <br/> |facultatif  <br/> |Représente une unité de mesure par défaut est la liste de distribution.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |XSD : String  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |La valeur de la cellule de feuille ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Remarques

L’attribut **N** de cet élément de **cellule** doit être un ensemble limité de valeurs qui correspondent à des cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet élément de **cellule** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|X   <br/> |Coordonnée x du sommet de fin d’un arc par rapport à la largeur de la forme.  <br/> |[Ligne RelEllipticalArcTo (section Géométrie)](relellipticalarcto-row-geometry-section.md) <br/> |
|Y  <br/> |Coordonnée y du sommet de fin d’un arc par rapport à la hauteur de la forme.  <br/> |[Ligne RelEllipticalArcTo (section Géométrie)](relellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |La coordonnée x du contrôle de l’arc point par rapport à la largeur de la forme ; un point sur l’arc.  <br/> |[Ligne RelEllipticalArcTo (section Géométrie)](relellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |Point de la coordonnée y du contrôle d’un arc par rapport à la largeur de la forme.  <br/> |[Ligne RelEllipticalArcTo (section Géométrie)](relellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |Angle du grand axe d’un arc par rapport à l’axe x de son parent.  <br/> |[Ligne RelEllipticalArcTo (section Géométrie)](relellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |Le taux de grand axe d’un arc à l’axe secondaire.  <br/> |[Ligne RelEllipticalArcTo (section Géométrie)](relellipticalarcto-row-geometry-section.md) <br/> |
   

