---
title: ComplexType DocumentSheet_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: a1f51ef6f0340b4430860eabde3ad778e923fed0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326137"
---
# <a name="documentsheettype-complextype-visio-xml"></a>ComplexType DocumentSheet_Type ('Visio XML')

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Base d’extension** <br/> |Sheet_Type  <br/> |
   
## <a name="definition"></a>Définition

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
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
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |xsd: Boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd: Boolean.  <br/> |
|IsCustomNameU  <br/> |xsd: Boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd: Boolean.  <br/> |
|Nom  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
|NameU  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
|UniqueID  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
   

