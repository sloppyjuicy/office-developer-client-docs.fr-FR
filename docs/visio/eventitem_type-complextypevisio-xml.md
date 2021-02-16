---
title: EventItem_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f157db03-e7d0-d39f-cbde-2a22f45b40ed
ms.openlocfilehash: f0fd618cc2a86d3695d0d6f6c446f118475ffc1f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541791"
---
# <a name="eventitem_type-complextype-visio-xml"></a>EventItem_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
      <xs:complexType name="EventItem_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Action"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="EventCode"
  type="xsd:unsignedShort"
     use="required"
    />
    <xs:attribute name="Enabled"
  type="xsd:boolean"
    />
    <xs:attribute name="Target"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="TargetArgs"
  type="xsd:string"
     use="required"
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
|Action  <br/> |xsd:unsignedShort  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedShort.  <br/> |
|Activé  <br/> |xsd:boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd:boolean.  <br/> |
|EventCode  <br/> |xsd:unsignedShort  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedShort.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|Target  <br/> |xsd:string  <br/> |obligatoire  <br/> ||Valeurs du type xsd:string.  <br/> |
|TargetArgs  <br/> |xsd:string  <br/> |obligatoire  <br/> ||Valeurs du type xsd:string.  <br/> |
   

