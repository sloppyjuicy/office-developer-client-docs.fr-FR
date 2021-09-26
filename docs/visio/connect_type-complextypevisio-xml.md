---
title: Connect_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 24993072beee1542244603c7943fee9517d36ec9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612994"
---
# <a name="connect_type-complextype-visio-xml"></a>Connect_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
      <xs:complexType name="Connect_Type">
    <xs:attribute name="FromSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FromCell"
  type="xsd:string"
    />
    <xs:attribute name="FromPart"
  type="xsd:int"
    />
    <xs:attribute name="ToSheet"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ToCell"
  type="xsd:string"
    />
    <xs:attribute name="ToPart"
  type="xsd:int"
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
|FromCell  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string.  <br/> |
|FromPart  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int.  <br/> |
|FromSheet  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|ToCell  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string.  <br/> |
|ToPart  <br/> |xsd:int  <br/> |facultatif  <br/> ||Valeurs du type xsd:int.  <br/> |
|ToSheet  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
   

