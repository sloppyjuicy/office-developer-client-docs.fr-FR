---
title: ComplexType Connect_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2230976b-f2a8-425b-b8b0-a7fd5efb4536
ms.openlocfilehash: 158fad1f3ec18bbc9565229338f4710c145c17e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327082"
---
# <a name="connecttype-complextype-visio-xml"></a>ComplexType Connect_Type ('Visio XML')

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
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

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|FromCell  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
|FromPart  <br/> |xsd: int  <br/> |facultatif  <br/> ||Valeurs du type xsd: int.  <br/> |
|FromSheet  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
|ToCell  <br/> |xsd: String  <br/> |facultatif  <br/> ||Valeurs du type xsd: String.  <br/> |
|ToPart  <br/> |xsd: int  <br/> |facultatif  <br/> ||Valeurs du type xsd: int.  <br/> |
|ToSheet  <br/> |xsd: unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd: unsignedInt.  <br/> |
   

