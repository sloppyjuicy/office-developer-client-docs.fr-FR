---
title: Élément de cellule (section Geometry) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 82dcad38-d5fa-4892-91d9-1f3f25f1e600
description: Définit les propriétés qui déterminent la mise en forme et les propriétés comportementales par rapport aux lignes et aux arcs qui font la section Geometry.
ms.openlocfilehash: 838b7f20eab82718c2f8df21ae0b0037e76961db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628702"
---
# <a name="cell-element-geometry-section-visio-xml"></a>Élément de cellule (section Geometry) (Visio XML)

Définit les propriétés qui déterminent la mise en forme et les propriétés comportementales par rapport aux lignes et aux arcs qui font la section Geometry.
  
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Élément Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[Geometry_Type](geometry_type-complextypevisio-xml.md) <br/> |Définit les propriétés qui déterminent la mise en forme et les propriétés comportementales par rapport aux lignes et aux arcs qui font la section Geometry.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
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
|NoFill  <br/> |Indique si un chemin peut être rempli.  <br/> |[NoFill, cellule (section Geometry)](nofill-cell-geometry-section.md) <br/> |
|NoLine  <br/> |Détermine si un trait est tracé autour du contour du chemin.  <br/> |[NoLine, cellule (section Geometry)](noline-cell-geometry-section.md) <br/> |
|NoQuickDrag  <br/> |Détermine si une forme peut être sélectionnée ou glissée lorsque l’utilisateur clique sur la zone remplie définie par la section Geometry.  <br/> |[NoQuickDrag Cell (Geometry Section)](noquickdrag-cell-geometry-section.md) <br/> |
|NoShow  <br/> |Indique si un chemin est affiché sur la page de dessin.  <br/> |[NoShow, cellule (section Geometry)](noshow-cell-geometry-section.md) <br/> |
|NoSnap  <br/> |Détermine si les autres formes s'alignent sur un chemin.  <br/> |[NoSnap, cellule (section Geometry)](nosnap-cell-geometry-section.md) <br/> |
   

