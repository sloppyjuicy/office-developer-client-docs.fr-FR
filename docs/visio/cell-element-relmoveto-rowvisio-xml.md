---
title: Élément de cellule (ligne RelMoveTo) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8e91497c-0aa1-2021-9317-cf989e5b84a3
description: Contient les coordonnées x ou y du premier sommet d’une forme, ou les coordonnées x ou y du premier sommet après une coupure dans un chemin d’accès, par rapport à la hauteur et à la largeur de la forme.
ms.openlocfilehash: 12d0690b7a68fc1773747d3fb9075f6aaabfca05
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448698"
---
# <a name="cell-element-relmoveto-row-visio-xml"></a>Élément de cellule (ligne RelMoveTo) (Visio XML)

Contient les coordonnées x ou y du premier sommet d’une forme, ou les coordonnées x ou y du premier sommet après une coupure dans un chemin d’accès, par rapport à la hauteur et à la largeur de la forme.
  
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
|[Élément Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelMoveTo_Type](relmoveto_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y du premier sommet d’une forme, ou les coordonnées x ou y du premier sommet après une coupure dans un chemin d’accès, par rapport à la hauteur et à la largeur de la forme. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Spécifie une référence à une page. |
   
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
|X  <br/> |Si la **ligne RelMoveTo** est la première ligne de la section, la cellule X représente la coordonnée **x** du premier sommet d’une forme par rapport à la largeur de la forme. Si la **ligne RelMoveTo** apparaît entre deux lignes, la cellule **X** représente la coordonnée x du premier sommet après la rupture du chemin d’accès. |[RelMoveTo Row (Geometry Section)](relmoveto-row-geometry-section.md) <br/> |
|v  <br/> |Si la **ligne RelMoveTo** est la première ligne de la section, la cellule Y représente la coordonnée **y** du premier sommet d’une forme par rapport à la hauteur de la forme. Si la **ligne RelMoveTo** apparaît entre deux lignes, la cellule **Y** représente la coordonnée y du premier sommet après la rupture du chemin d’accès. |[RelMoveTo Row (Geometry Section)](relmoveto-row-geometry-section.md) <br/> |
   

