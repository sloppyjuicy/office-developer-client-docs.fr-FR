---
title: Type complexe StyleSheet_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 19440ab1365ff82bd37d705115fd123dcb630aba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396000"
---
# <a name="stylesheettype-complextype-visio-xml"></a>Type complexe StyleSheet_Type (« Visio XML »)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Sheet_Type  <br/> |
   
## <a name="definition"></a>Définition

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
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
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> ||Valeurs du type de type xsd : Boolean.  <br/> |
|IsCustomNameU  <br/> |type xsd : Boolean  <br/> |facultatif  <br/> ||Valeurs du type de type xsd : Boolean.  <br/> |
|Nom  <br/> |XSD : String  <br/> |facultatif  <br/> ||Valeurs du type xsd : String.  <br/> |
|NameU  <br/> |XSD : String  <br/> |facultatif  <br/> ||Valeurs du type xsd : String.  <br/> |
   

