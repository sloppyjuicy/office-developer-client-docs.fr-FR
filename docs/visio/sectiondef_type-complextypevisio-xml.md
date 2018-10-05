---
title: Type complexe SectionDef_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 1d13cf54861435aea2ce0b3aade955575d538891
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395076"
---
# <a name="sectiondeftype-complextype-visio-xml"></a>Type complexe SectionDef_Type (« Visio XML »)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucune  <br/> |
   
## <a name="definition"></a>Définition

```XML
          <xs:complexType name="SectionDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowDef"  type="RowDef_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|CellDef <br/> |[CellDef_Type](celldef_type-complextypevisio-xml.md) <br/> ||
|RowDef <br/> |[RowDef_Type](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |XSD : String  <br/> |obligatoire  <br/> ||Valeurs du type xsd : String.  <br/> |
|S  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|T  <br/> |XSD : String  <br/> |facultatif  <br/> ||Valeurs du type xsd : String.  <br/> |
   

