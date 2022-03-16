---
title: Élément de cellule (ligne Controls) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Contient une propriété pour un handle de contrôle particulier défini pour une forme.
ms.openlocfilehash: eb6156a89a7a3f850bb5a733f76560993b0de440
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506995"
---
# <a name="cell-element-controls-row-visio-xml"></a>Élément de cellule (ligne Controls) (Visio XML)

Contient une propriété pour un handle de contrôle particulier défini pour une forme.
  
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
|[Row, élément (section Controls)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Contient une propriété pour un handle de contrôle particulier défini pour une forme. |
   
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
|CanGlue  <br/> |Détermine si une poignée de contrôle peut être collée à d'autres formes. |[Can Glue, cellule (section Controls)](can-glue-cell-controls-section.md) <br/> |
|Invite  <br/> |Représente une chaîne de texte descriptive qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme. |[Tip, cellule (section Controls)](tip-cell-controls-section.md) <br/> |
|X  <br/> |Représente la coordonnée x qui indique l'emplacement de la poignée de contrôle d'une forme. Cette coordonnée est exprimée en système de coordonnées locales. |[X, cellule (section Controls)](x-cell-controls-section.md) <br/> |
|xCon  <br/> |Spécifie le type de comportement de la coordonnée x de la poignée de contrôle une fois le handle déplacé. |Aucun. |
|xDyn  <br/> |Représente la coordonnée x du point d'ancrage d'une poignée de contrôle. Cette coordonnée est exprimée en système de coordonnées locales. |[X Dynamics, cellule (section Controls)](x-dynamics-cell-controls-section.md) <br/> |
|v  <br/> |Représente la coordonnée y qui indique l'emplacement de la poignée de contrôle d'une forme. Cette coordonnée est exprimée en système de coordonnées locales. |[Y, cellule (section Controls)](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Spécifie le type de comportement de la coordonnée y de la poignée de contrôle une fois le handle déplacé. |Aucun. |
|YDyn  <br/> |Représente la coordonnée y du point d'ancrage d'une poignée de contrôle. Cette coordonnée est exprimée dans le système de coordonnées locales. |[Y Dynamics, cellule (section Controls)](y-dynamics-cell-controls-section.md) <br/> |
   

