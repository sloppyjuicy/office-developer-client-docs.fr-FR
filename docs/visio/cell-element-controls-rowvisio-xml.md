---
title: Élément de cellule (ligne contrôles) («Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Contient une propriété pour une poignée de contrôle spécifique définie pour une forme.
ms.openlocfilehash: ea54865a645486dfba53688278cb380142899d77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356090"
---
# <a name="cell-element-controls-row-visio-xml"></a>Élément de cellule (ligne contrôles) («Visio XML»)

Contient une propriété pour une poignée de contrôle spécifique définie pour une forme.
  
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
|[Élément de ligne (section contrôles)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Contient une propriété pour une poignée de contrôle spécifique définie pour une forme.  <br/> |
   
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
|CanGlue  <br/> |Détermine si une poignée de contrôle peut être collée à d'autres formes.  <br/> |[Can Glue, cellule (section Controls)](can-glue-cell-controls-section.md) <br/> |
|Invite  <br/> |Représente une chaîne de texte descriptive qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme.  <br/> |[Tip, cellule (section Controls)](tip-cell-controls-section.md) <br/> |
|X  <br/> |Représente la coordonnée x qui indique l'emplacement de la poignée de contrôle d'une forme. Cette coordonnée est exprimée en système de coordonnées locales.  <br/> |[X, cellule (section Controls)](x-cell-controls-section.md) <br/> |
|xCon  <br/> |Spécifie le type de comportement de la coordonnée x de la poignée de contrôle après le déplacement de la poignée.  <br/> |Aucun.  <br/> |
|xDyn  <br/> |Représente la coordonnée x du point d'ancrage d'une poignée de contrôle. Cette coordonnée est exprimée en système de coordonnées locales.  <br/> |[X Dynamics, cellule (section Controls)](x-dynamics-cell-controls-section.md) <br/> |
|v  <br/> |Représente la coordonnée y qui indique l'emplacement de la poignée de contrôle d'une forme. Cette coordonnée est exprimée en système de coordonnées locales.  <br/> |[Y, cellule (section Controls)](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Spécifie le type de comportement de la coordonnée y de la poignée de contrôle après le déplacement de la poignée.  <br/> |Aucun.  <br/> |
|YDyn  <br/> |Représente la coordonnée y du point d'ancrage d'une poignée de contrôle. Cette coordonnée est exprimée dans le système de coordonnées locales.  <br/> |[Y Dynamics, cellule (section Controls)](y-dynamics-cell-controls-section.md) <br/> |
   

