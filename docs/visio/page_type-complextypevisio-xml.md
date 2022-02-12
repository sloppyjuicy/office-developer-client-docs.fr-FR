---
title: Page_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: 4e75c57cedd9579d7efa6ea3638fd83cda707273
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784767"
---
# <a name="page_type-complextype-visio-xml"></a>Page_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucune  <br/> |
   
## <a name="definition"></a>Définition

```XML
          <xs:complexType name="Page_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Background"
  type="xsd:boolean"
    />
    <xs:attribute name="BackPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
    <xs:attribute name="ReviewerID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AssociatedPage"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-page_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AssociatedPage  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|Contexte  <br/> |xsd:boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd:boolean. |
|BackPage  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt. |
|IsCustomName  <br/> |xsd:boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd:boolean. |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd:boolean. |
|Nom  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string. |
|NameU  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string. |
|ReviewerID  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt. |
|ViewCenterX  <br/> |xsd:double  <br/> |facultatif  <br/> ||Valeurs du type xsd:double. |
|ViewCenterY  <br/> |xsd:double  <br/> |facultatif  <br/> ||Valeurs du type xsd:double. |
|ViewScale  <br/> |xsd:double  <br/> |facultatif  <br/> ||Valeurs du type xsd:double. |
   

