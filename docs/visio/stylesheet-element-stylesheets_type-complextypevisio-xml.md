---
title: Élément StyleSheet (StyleSheets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: Représente un style défini dans un document.
ms.openlocfilehash: 4a05a6c2b94f8080c339f203497995ac5c72e562
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622766"
---
# <a name="stylesheet-element-stylesheets_type-complextype-visio-xml"></a>Élément StyleSheet (StyleSheets_Type complexType) (Visio XML)

Représente un style défini dans un document.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Composants de document** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[StyleSheets](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Contient une collection **d’éléments StyleSheet** pour le document.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une propriété unique.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Spécifie une collection de propriétés connexes.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de l’élément StyleSheet dont ce style hérite de la mise en forme du remplissage.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> |ID unique de l’élément au sein de son élément parent.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si le nom a été personnalisé par l’utilisateur.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |facultatif  <br/> |Indique si le nom universel a été personnalisé par l’utilisateur.  <br/> |Valeurs du type xsd:boolean.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de l’élément StyleSheet dont ce style hérite de la mise en forme des lignes.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom de l’élément.  <br/> |Valeurs du type xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |facultatif  <br/> |Nom universel de l’élément.  <br/> |Valeurs du type xsd:string.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> |ID de l’élément StyleSheet dont ce style hérite de la mise en forme du texte.  <br/> |Valeurs du type xsd:unsignedInt.  <br/> |
   

