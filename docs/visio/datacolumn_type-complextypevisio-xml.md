---
title: DataColumn_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: a8efaf7e7f6a724e7e4165328ce27152f5f65833
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448474"
---
# <a name="datacolumn_type-complextype-visio-xml"></a>DataColumn_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

||Valeur |
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Calendrier  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedShort. |
|ColumnNameID  <br/> |xsd:string  <br/> |obligatoire  <br/> ||Valeurs du type xsd:string. |
|Devise  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedShort. |
|DataType  <br/> |xsd:unsignedShort  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedShort. |
|Degree  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|Hyperlink  <br/> |xsd:boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd:boolean. |
|Étiquette  <br/> |xsd:string  <br/> |obligatoire  <br/> ||Valeurs du type xsd:string. |
|LangID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|Mappée  <br/> |xsd:boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd:boolean. |
|Nom  <br/> |xsd:string  <br/> |obligatoire  <br/> ||Valeurs du type xsd:string. |
|OrigLabel  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string. |
|UnitType  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string. |
   

