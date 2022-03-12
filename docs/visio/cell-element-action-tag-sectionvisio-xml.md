---
title: Élément de cellule (section Action Tag) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Définit une propriété pour une balise d’action sur une forme ou une page.
ms.openlocfilehash: 0080643f5c62cfbde4d290d34eb0f3df52589c2e
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448600"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Élément de cellule (section Action Tag) (Visio XML)

Définit une propriété pour une balise d’action sur une forme ou une page.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
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
|[Row, élément (section ActionTag)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |Définit une balise d’action sur une forme ou une page. |
   
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
|ButtonFace  <br/> |Contient l’ID de l’image de la face de bouton qui s’affiche sur le bouton de balise d’action. |[ButtonFace, cellule (section Action Tags)](buttonface-cell-action-tags-section.md) <br/> |
|Description  <br/> |Contient une chaîne qui décrit la balise d’action, qui s’affiche sous forme d’info-bulle lorsque l’utilisateur place le pointeur sur la balise. |[Description, cellule (section Action Tags)](description-cell-action-tags-section.md) <br/> |
|Désactivé  <br/> |Indique si la balise d’action s’affiche dans la fenêtre de dessin. |[Disabled, cellule (section Action Tags)](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Détermine si la balise d’action s’affiche lorsque l’utilisateur place le pointeur sur la balise, lorsque la forme est sélectionnée ou en tout temps. |[DisplayMode, cellule (Section Action Tags)](displaymode-cell-action-tags-section.md) <br/> |
|TagName  <br/> |Nom de la balise d’action utilisé comme référence pour associer la balise d’action à ses actions. |[TagName, cellule (section Action Tags)](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |Position de la coordonnée x dans le système de coordonnées locales de la forme et autour de laquelle est positionné le bouton de balise d’action. |[X, cellule (section Action Tags)](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |Décalage x du bouton de balise d’action par rapport au point défini par les cellules X et Y. |[X Justify, cellule (section Action Tags)](x-justify-cell-action-tags-section.md) <br/> |
|v  <br/> |Position de la coordonnée y dans le système de coordonnées locales de la forme et autour de laquelle est positionné le bouton de balise d’action. |[Y, cellule (section Action Tags)](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |Décalage y du bouton de balise d’action par rapport au point défini par les cellules X et Y. |[Y Justify, cellule (section Action Tags)](y-justify-cell-action-tags-section.md) <br/> |
   

