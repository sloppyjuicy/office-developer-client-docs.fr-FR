---
title: DataRecordSet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: b2e2a1086f27ced49f5d81b6ed6f4277194b5bed
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787400"
---
# <a name="datarecordset_type-complextype-visio-xml"></a>DataRecordSet_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucune  <br/> |
   
## <a name="definition"></a>Définition

```XML
          <xs:complexType name="DataRecordSet_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DataColumns"  type="DataColumns_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PrimaryKey"  type="PrimaryKey_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowMap"  type="RowMap_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshConflict"  type="RefreshConflict_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="AutoLinkComparison"  type="AutoLinkComparison_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ConnectionID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="Options"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TimeRefreshed"
  type="xsd:dateTime"
    />
    <xs:attribute name="NextRowID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="RowOrder"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshOverwriteAll"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshNoReconciliationUI"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshInterval"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReplaceLinks"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Checksum"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> ||
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Somme de contrôle  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|Commande  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string. |
|ConnectionID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt. |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string. |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|Options  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|RefreshInterval  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|RefreshNoRecontermtionUI  <br/> |xsd:boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd:boolean. |
|RefreshOverwriteAll  <br/> |xsd:boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd:boolean. |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|RowOrder  <br/> |xsd:boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd:boolean. |
|TimeRefreshed  <br/> |xsd:dateTime  <br/> |facultatif  <br/> ||Valeurs du type xsd:dateTime. |
   

