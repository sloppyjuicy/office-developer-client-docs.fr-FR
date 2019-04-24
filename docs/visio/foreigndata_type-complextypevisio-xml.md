---
title: ComplexType ForeignData_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346010"
---
# <a name="foreigndatatype-complextype-visio-xml"></a>ComplexType ForeignData_Type ('Visio XML')

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
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

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[Ver](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd: double  <br/> |facultatif  <br/> ||Valeurs du type xsd: double.  <br/> |
|CompressionType  <br/> |xsd: Token  <br/> |facultatif  <br/> ||Valeurs du type xsd: Token.  <br/> |
|ExtentX  <br/> |xsd: double  <br/> |facultatif  <br/> ||Valeurs du type xsd: double.  <br/> |
|Étendue  <br/> |xsd: double  <br/> |facultatif  <br/> ||Valeurs du type xsd: double.  <br/> |
|ForeignType  <br/> |xsd: Token  <br/> |obligatoire  <br/> ||Valeurs du type xsd: Token.  <br/> |
|MappingMode  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd: double  <br/> |facultatif  <br/> ||Valeurs du type xsd: double.  <br/> |
|ObjectType  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
|ObjectWidth  <br/> |xsd: double  <br/> |facultatif  <br/> ||Valeurs du type xsd: double.  <br/> |
|ShowAsIcon  <br/> |xsd: Boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd: Boolean.  <br/> |
   

