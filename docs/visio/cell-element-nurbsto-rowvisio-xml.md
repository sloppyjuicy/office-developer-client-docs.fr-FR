---
title: Élément de cellule (ligne NURBSTo) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e76bae8f-b9de-39ef-1f56-b00a6cd2ba6c
description: Contient les coordonnées x ou y, la position du deuxième au dernier nœud, la position du dernier poids, la position du premier nœud, la position de la première pondération ou la formule d’une ligne B-spline rationnelle nonuniforme (NURBS).
ms.openlocfilehash: 8b17fc8bfcda34ed8a725bf1ba1911f2e593046b
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448446"
---
# <a name="cell-element-nurbsto-row-visio-xml"></a>Élément de cellule (ligne NURBSTo) (Visio XML)

Contient les coordonnées x ou y, la position du deuxième au dernier nœud, la position du dernier poids, la position du premier nœud, la position de la première pondération ou la formule d’une ligne B-spline rationnelle nonuniforme (NURBS).
  
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
|[Élément Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[NURBSTo_Type](nurbsto_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, la position du deuxième au dernier nœud, la position du dernier poids, la position du premier nœud, la position de la première pondération ou la formule d’une ligne B-spline rationnelle nonuniforme (NURBS). |
   
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
|X  <br/> |Coordonnée x du dernier point de contrôle d'une courbe NURBS. |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|v  <br/> |Coordonnée y du dernier point de contrôle d'une courbe NURBS. |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|A  <br/> |Avant-dernier nœud de la courbe NURBS. |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|B  <br/> |La dernière épaisseur de la courbe NURBS. |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|C  <br/> |Le premier nœud de la courbe NURBS. |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|D  <br/> |La première épaisseur de la courbe NURBS. |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|E  <br/> |Une formule de courbe NURBS. |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
   

