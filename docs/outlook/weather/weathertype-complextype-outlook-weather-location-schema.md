---
title: complexType weatherType (outlook weather location schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Définit les paramètres sur les conditions météorologiques d’un emplacement.
ms.openlocfilehash: f7d33cb018daf4ece2ba468b9ebe92b0fc7b1545
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542918"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a>complexType weatherType (outlook weather location schema)

Définit les paramètres sur les conditions météorologiques d’un emplacement.
  
## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Fichier de schéma** <br/> |getweatherlocation.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un code associé à l’emplacement pour distinguer plusieurs emplacements du même nom.  <br/> |Valeur du type xs:string  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie le nom de l’emplacement.  <br/> |Valeur du type xs:string  <br/> |
   

