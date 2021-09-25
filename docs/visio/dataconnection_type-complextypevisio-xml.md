---
title: DataConnection_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 8d0020f26a3b8360e4af0194310f9a137717d415
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563069"
---
# <a name="dataconnection_type-complextype-visio-xml"></a>DataConnection_Type complexType (Visio XML)

## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Fichier de schéma** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
      <xs:complexType name="DataConnection_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FileName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ConnectionString"
  type="xsd:string"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="FriendlyName"
  type="xsd:string"
    />
    <xs:attribute name="Timeout"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AlwaysUseConnectionFile"
  type="xsd:boolean"
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
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |facultatif  <br/> ||Valeurs du type xsd:boolean.  <br/> |
|Commande  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string.  <br/> |
|ConnectionString  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string.  <br/> |
|FileName  <br/> |xsd:string  <br/> |obligatoire  <br/> ||Valeurs du type xsd:string.  <br/> |
|FriendlyName  <br/> |xsd:string  <br/> |facultatif  <br/> ||Valeurs du type xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obligatoire  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
|Délai d’expiration  <br/> |xsd:unsignedInt  <br/> |facultatif  <br/> ||Valeurs du type xsd:unsignedInt.  <br/> |
   

