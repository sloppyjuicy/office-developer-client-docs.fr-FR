---
title: Élément de cellule (ligne Controls) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Contient une propriété pour une poignée de contrôle particulière définie pour une forme.
ms.openlocfilehash: 45759522218736ddb6b08c3fd989658e08145fba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615983"
---
# <a name="cell-element-controls-row-visio-xml"></a>Élément de cellule (ligne Controls) (Visio XML)

Contient une propriété pour une poignée de contrôle particulière définie pour une forme.
  
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
|[Row, élément (section Controls)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Contient une propriété pour une poignée de contrôle particulière définie pour une forme.  <br/> |
   
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
|CanGlue  <br/> |Détermine si une poignée de contrôle peut être collée à d'autres formes.  <br/> |[Can Glue, cellule (section Controls)](can-glue-cell-controls-section.md) <br/> |
|Invite  <br/> |Représente une chaîne de texte descriptive qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme.  <br/> |[Tip, cellule (section Controls)](tip-cell-controls-section.md) <br/> |
|X  <br/> |Représente la coordonnée x qui indique l'emplacement de la poignée de contrôle d'une forme. Cette coordonnée est exprimée en système de coordonnées locales.  <br/> |[X, cellule (section Controls)](x-cell-controls-section.md) <br/> |
|xCon  <br/> |Spécifie le type de comportement de la coordonnée x de la poignée de contrôle une fois le handle déplacé.  <br/> |Aucun.  <br/> |
|xDyn  <br/> |Représente la coordonnée x du point d'ancrage d'une poignée de contrôle. Cette coordonnée est exprimée en système de coordonnées locales.  <br/> |[X Dynamics, cellule (section Controls)](x-dynamics-cell-controls-section.md) <br/> |
|O  <br/> |Représente la coordonnée y qui indique l'emplacement de la poignée de contrôle d'une forme. Cette coordonnée est exprimée en système de coordonnées locales.  <br/> |[Y, cellule (section Controls)](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Spécifie le type de comportement de la coordonnée y de la poignée de contrôle une fois le handle déplacé.  <br/> |Aucun.  <br/> |
|YDyn  <br/> |Représente la coordonnée y du point d'ancrage d'une poignée de contrôle. Cette coordonnée est exprimée dans le système de coordonnées locales.  <br/> |[Y Dynamics, cellule (section Controls)](y-dynamics-cell-controls-section.md) <br/> |
   

