---
title: ComplexType HeaderFooterFont_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335622"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a>ComplexType HeaderFooterFont_Type ('Visio XML')

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
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

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedByte.  <br/> |
|Échappement  <br/> |xsd: int  <br/> |facultatif  <br/> ||Valeurs du type xsd: int.  <br/> |
|FaceName  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
|Hauteur  <br/> |xsd: int  <br/> |facultatif  <br/> ||Valeurs du type xsd: int.  <br/> |
|Italic  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedByte.  <br/> |
|Orientation  <br/> |xsd: int  <br/> |facultatif  <br/> ||Valeurs du type xsd: int.  <br/> |
|La précision  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedByte.  <br/> |
|Quality  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedByte.  <br/> |
|Barré  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedByte.  <br/> |
|Underline  <br/> |xsd: unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd: unsignedByte.  <br/> |
|Pondération  <br/> |xsd: int  <br/> |facultatif  <br/> ||Valeurs du type xsd: int.  <br/> |
|Largeur  <br/> |xsd: int  <br/> |facultatif  <br/> ||Valeurs du type xsd: int.  <br/> |
   

