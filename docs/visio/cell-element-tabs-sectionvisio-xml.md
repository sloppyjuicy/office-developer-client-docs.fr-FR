---
title: Élément de cellule (section Tabs) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4292d489-fb7c-9d5d-9bec-2a1a0772d8ba
description: Spécifie une propriété qui contrôle la position ou l’alignement des tabulations de forme et de style.
ms.openlocfilehash: 7627d563a6f3a742a5219929ee0cd73b703acee3
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63403373"
---
# <a name="cell-element-tabs-section-visio-xml"></a>Élément de cellule (section Tabs) (Visio XML)

Spécifie une propriété qui contrôle la position ou l’alignement des tabulations de forme et de style. 
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
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
|[Row, élément (tabs, section)](row-element-tabs-sectionvisio-xml.md) <br/> |[TabsRow_Type](tabsrow_type-complextypevisio-xml.md) <br/> |Spécifie une propriété qui contrôle la position ou l’alignement des tabulations de forme et de style. |
   
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
|Alignement  <br/> |Détermine l'alignement des tabulations. |[Alignment, cellule (section Tabs)](alignment-cell-tabs-section.md) <br/> |
|Position  <br/> |Définit la position d'une tabulation. La position de la tabulation est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la position de la tabulation ne change pas. |[Position, cellule (section Tabs)](position-cell-tabs-section.md) <br/> |
   

