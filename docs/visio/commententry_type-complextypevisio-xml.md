---
title: Type complexe CommentEntry_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 5ee3c9f2aa8b0af91289ce1cd6bb2355adec3426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788282"
---
# <a name="commententrytype-complextype-visio-xml"></a>Type complexe CommentEntry_Type (« Visio XML »)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |XSD : String  <br/> |
   
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

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|AutoCommentType  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|CommentID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|Date  <br/> |XSD : DateTime  <br/> |obligatoire  <br/> ||Valeurs du type xsd : DateTime.  <br/> |
|Terminé  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> ||Valeurs du type de type xsd : Boolean.  <br/> |
|EditDate  <br/> |XSD : DateTime  <br/> |facultatif  <br/> ||Valeurs du type xsd : DateTime.  <br/> |
|PageID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
   

