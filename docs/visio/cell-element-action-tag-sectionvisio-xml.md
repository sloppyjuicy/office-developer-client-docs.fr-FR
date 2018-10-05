---
title: Élément de cellule (Section balise d’Action) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Définit une propriété pour une balise d’action sur une forme ou une page.
ms.openlocfilehash: 61fad8575532adde0106ef6db2888fe38f3ae4b7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392500"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Élément de cellule (Section balise d’Action) (« Visio XML »)

Définit une propriété pour une balise d’action sur une forme ou une page.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |Masters.XML, maître # .xml, pages.xml, page # .xml  <br/> |
   
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
|[Row, élément (ActionTag Section)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |Définit une balise d’action sur une forme ou une page.  <br/> |
   
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
|ButtonFace  <br/> |Contient l’ID de l’image de la face de bouton qui s’affiche sur le bouton de balise d’action.  <br/> |[ButtonFace, cellule (section Action Tags)](buttonface-cell-action-tags-section.md) <br/> |
|Description  <br/> |Contient une chaîne qui décrit la balise d’action, qui s’affiche sous forme d’info-bulle lorsque l’utilisateur place le pointeur sur la balise.  <br/> |[Description, cellule (section Action Tags)](description-cell-action-tags-section.md) <br/> |
|Désactivé  <br/> |Indique si la balise d’action s’affiche dans la fenêtre de dessin.  <br/> |[Disabled, cellule (section Action Tags)](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Détermine si la balise d’action apparaît lorsque l’utilisateur déplace le pointeur au-dessus de la balise, quand la forme est sélectionnée ou tout le temps.  <br/> |[DisplayMode, cellule (Section Action Tags)](displaymode-cell-action-tags-section.md) <br/> |
|TagName  <br/> |Nom de la balise d’action utilisé comme référence pour associer la balise d’action à ses actions.  <br/> |[TagName, cellule (section Action Tags)](tagname-cell-action-tags-section.md) <br/> |
|X   <br/> |Position de la coordonnée x dans le système de coordonnées locales de la forme et autour de laquelle est positionné le bouton de balise d’action.  <br/> |[X, cellule (section Action Tags)](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |Décalage x du bouton de balise d’action par rapport au point défini par les cellules X et Y.  <br/> |[X Justify, cellule (section Action Tags)](x-justify-cell-action-tags-section.md) <br/> |
|Y  <br/> |Position de la coordonnée y dans le système de coordonnées locales de la forme et autour de laquelle est positionné le bouton de balise d’action.  <br/> |[Y, cellule (section Action Tags)](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |Décalage y du bouton de balise d’action par rapport au point défini par les cellules X et Y.  <br/> |[Y Justify, cellule (section Action Tags)](y-justify-cell-action-tags-section.md) <br/> |
   

