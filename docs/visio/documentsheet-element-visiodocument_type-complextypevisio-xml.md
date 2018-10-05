---
title: DocumentSheet, élément (VisioDocument_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Spécifie une structure DocumentSheet.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383463"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a>DocumentSheet, élément (VisioDocument_Type, complexType) (« Visio XML »)

Spécifie une structure DocumentSheet.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15.xsd  <br/> |
|**Parties de document** <br/> |document.Xml  <br/> |
   
## <a name="definition"></a>Définition

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
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
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Spécifie une cellule dans un DocumentSheet.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Indique si le nom a été personnalisé par l’utilisateur.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|IsCustomNameU  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> |Indique si le nom universel a été personnalisé par l’utilisateur.  <br/> |Valeurs du type de type xsd : Boolean.  <br/> |
|Nom  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le nom dépendant de la langue de la propriété DocumentSheet.  <br/> |Valeurs du type xsd : String.  <br/> |
|NameU  <br/> |XSD : String  <br/> |facultatif  <br/> |Spécifie le nom indépendant du langage de la propriété DocumentSheet.  <br/> |Valeurs du type xsd : String.  <br/> |
|UniqueID  <br/> |XSD : String  <br/> |facultatif  <br/> |Valeur string facultative. Un GUID (identificateur global unique) qui identifie la forme.  <br/> |Valeurs du type xsd : String.  <br/> |
   

