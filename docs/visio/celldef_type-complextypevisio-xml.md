---
title: CellDef_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ea346d-1786-dc87-073d-8e7459b7fef1
ms.openlocfilehash: 7b437e35aadfef0390908cb1337cc738668382e5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542295"
---
# <a name="celldef_type-complextype-visio-xml"></a>CellDef_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
      <xs:complexType name="CellDef_Type">
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="F"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|F  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string.  <br/> |
|IX  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|N  <br/> |xsd:string  <br/> |obligatoire  <br/> ||Valeurs du type xsd:string.  <br/> |
|S  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|T  <br/> |xsd:token  <br/> |obligatoire  <br/> ||Valeurs du type xsd:token.  <br/> |
   

