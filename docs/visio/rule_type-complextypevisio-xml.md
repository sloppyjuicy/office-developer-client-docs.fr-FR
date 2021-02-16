---
title: Rule_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d023139b-de1f-49f7-86d2-14a683bc5a46
ms.openlocfilehash: a1c3111458b90cd5e1b181a3b1776f64d8ec476b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541714"
---
# <a name="rule_type-complextype-visio-xml"></a>Rule_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
          <xs:complexType name="Rule_Type">
          
          <xs:sequence>
    <xs:element name="RuleFilter"  type="RuleFilter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleTest"  type="RuleTest_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Category"
  type="xsd:string"
    />
    <xs:attribute name="Description"
  type="xsd:string"
    />
    <xs:attribute name="RuleTarget"
  type="xsd:int"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> ||
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Catégorie  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string.  <br/> |
|Description  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|Ignoré  <br/> |xsd:boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd:boolean.  <br/> |
|NameU  <br/> |xsd:string  <br/> |obligatoire  <br/> ||Valeurs du type xsd:string.  <br/> |
|RuleTarget  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int.  <br/> |
   

