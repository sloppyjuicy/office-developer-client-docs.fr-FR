---
title: Type complexe Page_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401551"
---
# <a name="pagetype-complextype-visio-xml"></a>Type complexe Page_Type (« Visio XML »)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
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

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-page_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|AssociatedPage  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|Arrière-plan  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> ||Valeurs du type de type xsd : Boolean.  <br/> |
|BackPage  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> ||Valeurs du type de type xsd : Boolean.  <br/> |
|IsCustomNameU  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> ||Valeurs du type de type xsd : Boolean.  <br/> |
|Nom  <br/> |XSD : String  <br/> |facultatif  <br/> ||Valeurs du type xsd : String.  <br/> |
|NameU  <br/> |XSD : String  <br/> |facultatif  <br/> ||Valeurs du type xsd : String.  <br/> |
|ReviewerID  <br/> |XSD:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |XSD : double  <br/> |facultatif  <br/> ||Valeurs du type xsd : double.  <br/> |
|ViewCenterY  <br/> |XSD : double  <br/> |facultatif  <br/> ||Valeurs du type xsd : double.  <br/> |
|ViewScale  <br/> |XSD : double  <br/> |facultatif  <br/> ||Valeurs du type xsd : double.  <br/> |
   

