---
title: Élément de cellule (ligne RelQuadBezTo) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8b3aea70-a69f-a85e-83d8-c0fa2ee68836
description: Contient les coordonnées x ou y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme ou aux coordonnées x ou y du point de contrôle de la largeur et de la hauteur de la forme relative de courbe.
ms.openlocfilehash: 5d40d49d7544660e1a525834aeea05d67c1a2f80
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578073"
---
# <a name="cell-element-relquadbezto-row-visio-xml"></a>Élément de cellule (ligne RelQuadBezTo) (Visio XML)

Contient les coordonnées x ou y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme ou aux coordonnées x ou y du point de contrôle de la largeur et de la hauteur de la forme relative de courbe.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[Élément Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelQuadBezTo_Type](relquadbezto_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point de terminaison d’une courbe de Bézier quadratique par rapport à la largeur et à la hauteur de la forme ou aux coordonnées x ou y du point de contrôle de la largeur et de la hauteur de la forme relative de courbe.  <br/> |
   
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
|X  <br/> |Coordonnée x du sommet de fin d’une courbe de Bézier quadratique par rapport à la largeur de la forme.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|O  <br/> |Coordonnée y du sommet de fin d’une courbe de Bézier quadratique par rapport à la hauteur de la forme.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|A  <br/> |Coordonnée x du point de contrôle de la courbe par rapport à la largeur de la forme ; point sur l’arc. Le point de contrôle est mieux situé à mi-chemin entre les vertex de début et de fin de l’arc.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|B  <br/> |Coordonnée y du point de contrôle d’une courbe par rapport à la hauteur de la forme.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
   

