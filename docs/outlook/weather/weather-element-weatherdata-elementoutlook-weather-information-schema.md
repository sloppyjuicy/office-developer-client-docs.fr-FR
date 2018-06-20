---
title: météo élément (weatherdata) (schéma des informations météo Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Spécifie les conditions météorologiques d’un emplacement.
ms.openlocfilehash: c19db6657860dd35f90832aef0614f4fb88d87b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787792"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>météo élément (weatherdata) (schéma des informations météo Outlook)

Spécifie les conditions météorologiques d’un emplacement.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[WeatherData](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Définit l’élément météo.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[en cours](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie la météo.  <br/> |
|[prévision](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météo future d’au moins trois jours avance y compris aujourd'hui : aujourd'hui, demain, jour après demain.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|attribution  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie la source de la météo.  <br/> |Valeur du type xs : String  <br/> |
|degreetype  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie l’unité de la température de l’emplacement, par exemple, Celsius.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie l’URL de l’image pour l’emplacement.  <br/> |Valeur du type xs : String  <br/> |
|fuseau horaire  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie le décalage GMT.  <br/> |Une valeur comprise entre -11 et 12 inclus  <br/> |
|url  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie l’URL de la page web du service météo qui contient des informations météorologiques pour l’emplacement spécifié.  <br/> |Valeur du type xs : String  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie le code qui est associé à l’emplacement permet de distinguer plusieurs emplacement ayant le même nom.  <br/> |Valeur du type xs : String  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie le nom de l’emplacement qui s’affiche dans le contrôle de liste déroulante.  <br/> |Valeur du type xs : String  <br/> |
   

