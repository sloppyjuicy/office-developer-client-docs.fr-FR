---
title: Type complexe HeaderFooterFont_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397246"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a>Type complexe HeaderFooterFont_Type (« Visio XML »)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucune  <br/> |
   
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

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|Jeu de caractères  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|Échappement  <br/> |XSD : int  <br/> |facultatif  <br/> ||Valeurs du type xsd : int.  <br/> |
|Nom de la police  <br/> |XSD : String  <br/> |facultatif  <br/> ||Valeurs du type xsd : String.  <br/> |
|Height  <br/> |XSD : int  <br/> |facultatif  <br/> ||Valeurs du type xsd : int.  <br/> |
|Italique  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|Orientation  <br/> |XSD : int  <br/> |facultatif  <br/> ||Valeurs du type xsd : int.  <br/> |
|OutPrecision  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|Qualité  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|Barré  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|Souligné  <br/> |XSD:unsignedByte  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedByte.  <br/> |
|Pondération  <br/> |XSD : int  <br/> |facultatif  <br/> ||Valeurs du type xsd : int.  <br/> |
|Width  <br/> |XSD : int  <br/> |facultatif  <br/> ||Valeurs du type xsd : int.  <br/> |
   

