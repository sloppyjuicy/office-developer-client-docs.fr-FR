---
title: ComplexType DataColumn_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344701"
---
# <a name="datacolumntype-complextype-visio-xml"></a>ComplexType DataColumn_Type ('Visio XML')

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Calendrier  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd: String  <br/> |obligatoire  <br/> ||Valeurs du type xsd: String.  <br/> |
|Devise  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedShort.  <br/> |
|DataType  <br/> |xsd: unsignedShort  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedShort.  <br/> |
|Degree  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
|DisplayOrder  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
|DisplayWidth  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
|Lien hypertexte  <br/> |xsd: Boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd: Boolean.  <br/> |
|Étiquette  <br/> |xsd: String  <br/> |obligatoire  <br/> ||Valeurs du type xsd: String.  <br/> |
|ID  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
|Mappé  <br/> |xsd: Boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd: Boolean.  <br/> |
|Nom  <br/> |xsd: String  <br/> |obligatoire  <br/> ||Valeurs du type xsd: String.  <br/> |
|OrigLabel  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
|Type_d'unité  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
   

