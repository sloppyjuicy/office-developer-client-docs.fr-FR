---
title: HeaderFooterFont_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: 09eccf6dd9b71f5051138bff86a2124930c18350
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63403878"
---
# <a name="headerfooterfont_type-complextype-visio-xml"></a>HeaderFooterFont_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

||Valeur |
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte. |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte. |
|Escapement  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int. |
|FaceName  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string. |
|Hauteur  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int. |
|Italic  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte. |
|Orientation  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int. |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte. |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte. |
|Qualité  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte. |
|StrikeOut  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte. |
|Souligner  <br/> |xsd:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte. |
|Pondération  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int. |
|Largeur  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int. |
   

