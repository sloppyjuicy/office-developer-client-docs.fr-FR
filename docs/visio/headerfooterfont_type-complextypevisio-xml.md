---
title: HeaderFooterFont_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: 9f67e4aaecda4cc9260e357a9da6304f849abb77
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570497"
---
# <a name="headerfooterfont_type-complextype-visio-xml"></a>HeaderFooterFont_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
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
|CharSet  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|Escapement  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int.  <br/> |
|FaceName  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string.  <br/> |
|Hauteur  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int.  <br/> |
|Italic  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|Orientation  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int.  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|Qualité  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|StrikeOut  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|Souligner  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|Pondération  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int.  <br/> |
|Largeur  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int.  <br/> |
   

