---
title: Élément de cellule (section Geometry) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 82dcad38-d5fa-4892-91d9-1f3f25f1e600
description: Définit les propriétés qui déterminent la mise en forme et les propriétés comportementales par rapport aux lignes et aux arcs qui font la section Geometry.
ms.openlocfilehash: 5aeec35bd33a7b388e2f8580eded37cdfb0feb50
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426929"
---
# <a name="cell-element-geometry-section-visio-xml"></a>Élément de cellule (section Geometry) (Visio XML)

Définit les propriétés qui déterminent la mise en forme et les propriétés comportementales par rapport aux lignes et aux arcs qui font la section Geometry.
  
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
|[Élément Row (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[Geometry_Type](geometry_type-complextypevisio-xml.md) <br/> |Définit les propriétés qui déterminent la mise en forme et les propriétés comportementales par rapport aux lignes et aux arcs qui font la section Geometry. |
   
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
|NoFill  <br/> |Indique si un chemin peut être rempli. |[NoFill, cellule (section Geometry)](nofill-cell-geometry-section.md) <br/> |
|NoLine  <br/> |Détermine si un trait est tracé autour du contour du chemin. |[NoLine, cellule (section Geometry)](noline-cell-geometry-section.md) <br/> |
|NoQuickDrag  <br/> |Détermine si une forme peut être sélectionnée ou glissée lorsque l’utilisateur clique sur la zone remplie définie par la section Geometry. |[NoQuickDrag Cell (Geometry Section)](noquickdrag-cell-geometry-section.md) <br/> |
|NoShow  <br/> |Indique si un chemin est affiché sur la page de dessin. |[NoShow, cellule (section Geometry)](noshow-cell-geometry-section.md) <br/> |
|NoSnap  <br/> |Détermine si les autres formes s'alignent sur un chemin. |[NoSnap, cellule (section Geometry)](nosnap-cell-geometry-section.md) <br/> |
   

