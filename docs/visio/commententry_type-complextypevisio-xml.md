---
title: ComplexType CommentEntry_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334943"
---
# <a name="commententrytype-complextype-visio-xml"></a>ComplexType CommentEntry_Type ('Visio XML')

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Base d’extension** <br/> |xsd: String  <br/> |
   
## <a name="definition"></a>Définition

```XML
      <xs:complexType name="CommentEntry_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="AuthorID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Date"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="EditDate"
  type="xsd:dateTime"
    />
    <xs:attribute name="Done"
  type="xsd:boolean"
    />
    <xs:attribute name="CommentID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="AutoCommentType"
  type="xsd:unsignedInt"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Faut  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
|AutoCommentType  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
|CommentID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
|Date  <br/> |xsd: dateTime  <br/> |obligatoire  <br/> ||Valeurs du type xsd: dateTime.  <br/> |
|Terminé  <br/> |xsd: Boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd: Boolean.  <br/> |
|EditDate  <br/> |xsd: dateTime  <br/> |facultatif  <br/> ||Valeurs du type xsd: dateTime.  <br/> |
|PageID  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
|ShapeID  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
   

