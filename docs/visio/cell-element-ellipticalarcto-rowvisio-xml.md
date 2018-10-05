---
title: Élément de cellule (ligne EllipticalArcTo) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c0aa7a3-cc54-ffac-2c62-917b3d0a357e
description: Contient les coordonnées x ou y du point de terminaison d’un arc elliptique coordonnées x ou y du contrôle pointe sur l’arc, l’angle de l’axe x à l’axe majeur de l’ellipse ou rapport entre axes principaux et secondaires de l’ellipse.
ms.openlocfilehash: 22dc813108d8f7b5b517c298c40c73ead8d4eec4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395888"
---
# <a name="cell-element-ellipticalarcto-row-visio-xml"></a>Élément de cellule (ligne EllipticalArcTo) (« Visio XML »)

Contient les coordonnées x ou y du point de terminaison d’un arc elliptique coordonnées x ou y du contrôle pointe sur l’arc, l’angle de l’axe x à l’axe majeur de l’ellipse ou rapport entre axes principaux et secondaires de l’ellipse.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |master # .xml, page # .xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Row, élément (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[EllipticalArcTo_Type](ellipticalarcto_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’un arc elliptique coordonnées x ou y du contrôle pointe sur l’arc, l’angle de l’axe x à l’axe majeur de l’ellipse ou rapport entre axes principaux et secondaires de l’ellipse.  <br/> |
   
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
|X   <br/> |Coordonnée x du sommet de fin d'un arc.  <br/> |[EllipticalArcTo, ligne (section Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|Y  <br/> |Coordonnée y du sommet de fin d'un arc.  <br/> |[EllipticalArcTo, ligne (section Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |Coordonnée x du point de contrôle de l'arc (un point sur l'arc). La meilleure position pour le point de contrôle est environ le milieu entre les sommets de départ et de fin de l'arc. Sinon, l'arc peut prendre une taille extrême afin de passer par le point de contrôle, avec des résultats imprévisibles.  <br/> |[EllipticalArcTo, ligne (section Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |Coordonnée y du point de contrôle d’un arc.  <br/> |[EllipticalArcTo, ligne (section Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |Angle de l’axe de principal d’un arc par rapport à l’axe x de la forme parent.  <br/> |[EllipticalArcTo, ligne (section Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |Rapport entre l'axe majeur de l'arc et son axe mineur. Contrairement à la signification réelle de ces termes, l'axe « majeur » ne doit pas forcément être plus grand que l'axe « mineur ». Ce rapport peut donc être inférieur à 1. Si cette cellule a une valeur inférieure ou égale à 0, ou supérieure à 1000, les résultats sont imprévisibles.  <br/> |[EllipticalArcTo, ligne (section Geometry)](ellipticalarcto-row-geometry-section.md) <br/> |
   

