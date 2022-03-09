---
title: Élément de cellule (ligne Ellipse) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 210e6731-7c94-90b1-c7c4-635df974fdb6
description: Contient les coordonnées x ou y du point central de l’ellipse et deux points sur l’ellipse.
ms.openlocfilehash: 4c4b0d056c2f8266f382f7a53343cc0d714829e5
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405099"
---
# <a name="cell-element-ellipse-row-visio-xml"></a>Élément de cellule (ligne Ellipse) (Visio XML)

Contient les coordonnées x ou y du point central de l’ellipse et deux points sur l’ellipse.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[Ellipse_Type](ellipse_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du point central de l’ellipse et deux points sur l’ellipse. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page de dessin. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |facultatif  <br/> |Indique que la formule est évaluée à une erreur. La valeur de **E** est la valeur actuelle (chaîne de message d’erreur) ; la valeur de **l’attribut V** est la dernière valeur valide. |Chaîne de message d’erreur. |
|F  <br/> |xsd:string  <br/> |facultatif  <br/> | Représente la formule de l’élément. Cet attribut peut contenir l’une des chaînes suivantes :  <br/>  '(une formule)' si la formule existe localement  <br/>  `No Formula` si la formule est supprimée ou bloquée localement  <br/>  `Inh` si la formule est héritée. |Formule. |
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet. |Nom de la cellule ShapeSheet. Voir la section Remarques ci-dessous. |
|U  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente une unité de mesure La valeur par défaut est DL. |Unités de la cellule. |
|V  <br/> |xsd:string  <br/> |facultatif  <br/> |Représente la valeur de la cellule. |Valeur de la cellule ShapeSheet. |
   
## <a name="remarks"></a>Remarques

**L’attribut N** de cet **élément Cell** doit être l’un des ensembles limités de valeurs qui correspondent aux cellules ShapeSheet. Reportez-vous au tableau ci-dessous pour déterminer les valeurs de l’attribut **N** qui sont autorisées pour cet **élément Cell** . 
  
|**Valeur**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|X  <br/> |Coordonnée x du centre. |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|v  <br/> |Coordonnée y du centre. |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|A  <br/> |Coordonnée x du premier point sur l’ellipse ; associé à la coordonnée y représentée par la cellule B. |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|B  <br/> |Coordonnée y du premier point sur l’ellipse ; associé à la coordonnée x représentée par la cellule A. |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|C  <br/> |Coordonnée x du deuxième point sur l’ellipse ; associé à la coordonnée y représentée par la cellule D. |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
|D  <br/> |Coordonnée y du deuxième point sur l’ellipse ; associé à la coordonnée y représentée par la cellule C. |[Ellipse, ligne (section Geometry)](ellipse-row-geometry-section.md) <br/> |
   

