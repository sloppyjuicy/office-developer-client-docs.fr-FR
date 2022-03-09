---
title: PersonEntry_Type complexType (Visio XML)
ms.date: 02/18/2022
ms.openlocfilehash: 7dba1313783ae7daaee8de5724c909d3fc48bf82
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382489"
---
# <a name="personentry_type-complextype-visio-xml"></a>PersonEntry_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
            <xs:complexType name="PersonEntry_Type">
        <xs:sequence>
            <xs:any minOccurs="0" maxOccurs="unbounded" namespace="##any" processContents="lax" />
        </xs:sequence>
        <xs:attribute name="DisplayName" type="xs:string" use="required" />
        <xs:attribute name="PersonID" type="xs:unsignedInt" use="required" />
        <xs:attribute name="ProviderID" type="xs:string" />
        <xs:attribute name="UserID" type="xs:string" />
        <xs:anyAttribute namespace="##other" processContents="lax" />
    </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|DisplayName  <br/> |xsd:string  <br/> |obligatoire  <br/> ||Valeurs du type xsd:string. |
|PersonID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt. |
|ProviderID  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string. |
|UserID  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string. |
   

