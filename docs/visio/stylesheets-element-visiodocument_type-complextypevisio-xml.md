---
title: StyleSheets, élément (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da26de4b-3e5b-326b-de46-e8c542b74f02
description: Contient une collection d’éléments de feuille de style pour le document.
ms.openlocfilehash: 4aae3bcbecec34d961f2d14fd6d3865e7cd332f6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395825"
---
# <a name="stylesheets-element-visiodocumenttype-complextype-visio-xml"></a>StyleSheets, élément (VisioDocument_Type, complexType) (« Visio XML »)

Contient une collection d’éléments de feuille de style pour le document.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |L’élément racine d’un document Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Feuille de style](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Représente un style défini dans un document.  <br/> |
   
### <a name="attributes"></a>Attributs

Aucun.
  

