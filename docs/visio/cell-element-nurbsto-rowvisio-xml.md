---
title: Élément de cellule (ligne NURBSTo) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e76bae8f-b9de-39ef-1f56-b00a6cd2ba6c
description: Contient les coordonnées x ou y, la position de l'avant-dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur ou la formule pour une courbe B-spline rationnelle inuniforme (NURBS).
ms.openlocfilehash: f23f73d67d72f9536dc7ffe9e083058ea9306217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357693"
---
# <a name="cell-element-nurbsto-row-visio-xml"></a>Élément de cellule (ligne NURBSTo) ('Visio XML')

Contient les coordonnées x ou y, la position de l'avant-dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur ou la formule pour une courbe B-spline rationnelle inuniforme (NURBS).
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15. xsd  <br/> |
|**Parties de document** <br/> |Master #. xml, page #. Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément de ligne (géométrie)](row-element-geometry-sectionvisio-xml.md) <br/> |[NURBSTo_Type](nurbsto_type-complextypevisio-xml.md) <br/> |Contient les coordonnées x ou y, la position de l'avant-dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur ou la formule pour une courbe B-spline rationnelle inuniforme (NURBS).  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Cette énumération spécifie une référence à une page de dessin.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: String  <br/> |facultatif  <br/> |Indique que la formule génère une erreur. La valeur **E** est la valeur actuelle (chaîne de message d'erreur); la valeur de l'attribut **V** est la dernière valeur valide.  <br/> |Chaîne de message d'erreur.  <br/> |
|F  <br/> |xsd: String  <br/> |facultatif  <br/> | Représente la formule de l'élément. Cet attribut peut contenir l'une des chaînes suivantes:  <br/>  ' (une formule) 'si la formule existe localement  <br/>  `No Formula`Si la formule est supprimée ou bloquée localement  <br/>  `Inh`Si la formule est héritée.  <br/> |Une formule.  <br/> |
|N  <br/> |xsd: String  <br/> |obligatoire  <br/> |Représente le nom de la cellule ShapeSheet.  <br/> |Nom de la cellule ShapeSheet.  <br/> Consultez la section Remarques ci-dessous.  <br/> |
|U  <br/> |xsd: String  <br/> |facultatif  <br/> |Représente une unité de mesure la valeur par défaut est DL.  <br/> |Unités de la cellule.  <br/> |
|V  <br/> |xsd: String  <br/> |facultatif  <br/> |Représente la valeur de la cellule.  <br/> |Valeur de la cellule ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Remarques

L'attribut **N** de cet élément de **cellule** doit correspondre à l'un des jeux de valeurs limités qui correspondent aux cellules de la feuille ShapeSheet. RePortez-vous au tableau ci-dessous pour déterminer les valeurs de l'attribut **N** qui sont autorisées pour cet élément de **cellule** . 
  
|**Value**|**Description**|**Plus d’informations**|
|:-----|:-----|:-----|
|X  <br/> |Coordonnée x du dernier point de contrôle d'une courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|v  <br/> |Coordonnée y du dernier point de contrôle d'une courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|A  <br/> |Avant-dernier nœud de la courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|B  <br/> |La dernière épaisseur de la courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|C  <br/> |Le premier nœud de la courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|D  <br/> |La première épaisseur de la courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|E  <br/> |Une formule de courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
   

