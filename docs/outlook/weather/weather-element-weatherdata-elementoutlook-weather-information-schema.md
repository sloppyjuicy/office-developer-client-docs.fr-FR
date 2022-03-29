---
title: élément météo (élément weatherdata) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Spécifie les conditions météorologiques d’un emplacement.
ms.openlocfilehash: 8bb9ed8c835e1357c5bd572a6ffa3b8604fe4eb3
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455894"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>élément météo (élément weatherdata) (Outlook Weather Information Schema)

Spécifie les conditions météorologiques d’un emplacement.
  
## <a name="element-information"></a>Informations sur l'élément

|Propriété |Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[weatherdata](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Définit l’élément météo. |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[current](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météorologiques actuelles. |
|[forecast](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météorologiques futures d’au moins trois jours à l’avance, y compris aujourd’hui : Aujourd’hui, Demain, Jour après Demain. |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|attribution  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie la source des informations météorologiques. |Valeur du type xs:string  <br/> |
|degreetype  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie l’unité de température de l’emplacement, par exemple, Celsius. |C, F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie l’URL de l’image pour l’emplacement. |Valeur du type xs:string  <br/> |
|timezone  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie le décalage GMT. |Valeur entre -11 et 12 inclus  <br/> |
|url  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie l’URL de la page web du service météo qui contient des informations météorologiques pour l’emplacement spécifié. |Valeur du type xs:string  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie le code associé à l’emplacement utilisé pour distinguer plusieurs emplacements qui ont le même nom. |Valeur du type xs:string  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie le nom de l’emplacement qui apparaît dans le contrôle de la zone de baisse. |Valeur du type xs:string  <br/> |
   

