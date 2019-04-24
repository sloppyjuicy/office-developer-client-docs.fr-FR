---
title: ComplexType FaceName_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322553"
---
# <a name="facenametype-complextype-visio-xml"></a>ComplexType FaceName_Type ('Visio XML')

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
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
|Jeux de caractères  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
|Flags  <br/> |xsd: unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
|NameU  <br/> |xsd: String  <br/> |obligatoire  <br/> ||Valeurs du type xsd: String.  <br/> |
|Panos  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
|PaNose  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
|UnicodeRanges  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
   

