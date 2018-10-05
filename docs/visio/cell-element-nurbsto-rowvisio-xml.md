---
title: Élément de cellule (ligne NURBSTo) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e76bae8f-b9de-39ef-1f56-b00a6cd2ba6c
description: Contient la position x ou y coordonnées, du deuxième au dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur ou la formule d’une courbe B-spline rationnelle (NURBS).
ms.openlocfilehash: f23f73d67d72f9536dc7ffe9e083058ea9306217
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392801"
---
# <a name="cell-element-nurbsto-row-visio-xml"></a>Élément de cellule (ligne NURBSTo) (« Visio XML »)

Contient la position x ou y coordonnées, du deuxième au dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur ou la formule d’une courbe B-spline rationnelle (NURBS).
  
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
|[Row, élément (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[NURBSTo_Type](nurbsto_type-complextypevisio-xml.md) <br/> |Contient la position x ou y coordonnées, du deuxième au dernier nœud, la position de la dernière épaisseur, la position du premier nœud, la position de la première épaisseur ou la formule d’une courbe B-spline rationnelle (NURBS).  <br/> |
   
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
|X   <br/> |Coordonnée x du dernier point de contrôle d'une courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|Y  <br/> |Coordonnée y du dernier point de contrôle d'une courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|A  <br/> |Avant-dernier nœud de la courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|B  <br/> |La dernière épaisseur de la courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|C  <br/> |Le premier nœud de la courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|D  <br/> |La première épaisseur de la courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
|E  <br/> |Une formule de courbe NURBS.  <br/> |[NURBSTo, ligne (section Geometry)](nurbsto-row-geometry-section.md) <br/> |
   

