---
title: Type complexe Cell_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 38519bac-ce3e-9ded-d024-93dd7f34b107
ms.openlocfilehash: b17a251844a00ce01ad572dc63d971329214a23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788226"
---
# <a name="celltype-complextype-visio-xml"></a>Type complexe Cell_Type (« Visio XML »)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucune  <br/> |
   
## <a name="definition"></a>Définition

```XML
          <xs:complexType name="Cell_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="U"
  type="xsd:string"
    />
    <xs:attribute name="E"
  type="xsd:string"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="V"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD : String  <br/> |facultatif  <br/> ||Valeurs du type xsd : String.  <br/> |
|F  <br/> |XSD : String  <br/> |facultatif  <br/> ||Valeurs du type xsd : String.  <br/> |
|N  <br/> |XSD : String  <br/> |obligatoire  <br/> ||Valeurs du type xsd : String.  <br/> |
|U  <br/> |XSD : String  <br/> |facultatif  <br/> ||Valeurs du type xsd : String.  <br/> |
|V  <br/> |XSD : String  <br/> |facultatif  <br/> ||Valeurs du type xsd : String.  <br/> |
   

