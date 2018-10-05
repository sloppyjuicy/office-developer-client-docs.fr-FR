---
title: Type complexe ForeignData_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384156"
---
# <a name="foreigndatatype-complextype-visio-xml"></a>Type complexe ForeignData_Type (« Visio XML »)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucune  <br/> |
   
## <a name="definition"></a>Définition

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |XSD : double  <br/> |facultatif  <br/> ||Valeurs du type xsd : double.  <br/> |
|CompressionType  <br/> |XSD:Token  <br/> |facultatif  <br/> ||Valeurs du type xsd:token.  <br/> |
|ExtentX  <br/> |XSD : double  <br/> |facultatif  <br/> ||Valeurs du type xsd : double.  <br/> |
|ExtentY  <br/> |XSD : double  <br/> |facultatif  <br/> ||Valeurs du type xsd : double.  <br/> |
|ForeignType  <br/> |XSD:Token  <br/> |obligatoire  <br/> ||Valeurs du type xsd:token.  <br/> |
|MappingMode  <br/> |XSD:unsignedShort  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |XSD : double  <br/> |facultatif  <br/> ||Valeurs du type xsd : double.  <br/> |
|ObjectType  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |XSD : double  <br/> |facultatif  <br/> ||Valeurs du type xsd : double.  <br/> |
|ShowAsIcon  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> ||Valeurs du type de type xsd : Boolean.  <br/> |
   

