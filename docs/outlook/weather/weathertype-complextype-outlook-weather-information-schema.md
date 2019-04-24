---
title: complexType weatherType (schéma d'informations météorologiques Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Spécifie les conditions météorologiques d'un emplacement.
ms.openlocfilehash: ffa91c4982b5703041c79b47eb15a3a2b845b429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355040"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a>complexType weatherType (schéma d'informations météorologiques Outlook)

Spécifie les conditions météorologiques d'un emplacement.
  
## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |GetWeatherInfo. xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
## <a name="definition"></a>Définition

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[récent](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météorologiques actuelles.  <br/> |
|[prévisionnel](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météorologiques futures d'une avance de trois jours, y compris aujourd'hui: aujourd'hui, demain, jour après demain.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|attribution  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie la source des informations météorologiques.  <br/> |Une valeur du type xs: String  <br/> |
|degreetype  <br/> |XS: String  <br/> |obligatoire  <br/> |Indique l'unité de température de l'emplacement (par exemple, Celsius).  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie l'URL de l'image pour l'emplacement.  <br/> |Une valeur du type xs: String  <br/> |
|horaire  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Spécifie le décalage GMT.  <br/> |Une valeur comprise entre-11 et 12 inclus  <br/> |
|url  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie l'URL de la page Web du service météo qui contient des informations météorologiques pour l'emplacement spécifié.  <br/> |Une valeur du type xs: String  <br/> |
|weatherlocationcode  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie le code associé à l'emplacement utilisé pour distinguer plusieurs emplacements portant le même nom.  <br/> |Une valeur du type xs: String  <br/> |
|weatherlocationname  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie le nom de l'emplacement qui apparaît dans le contrôle de liste déroulante.  <br/> |Une valeur du type xs: String  <br/> |
   

