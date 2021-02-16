---
title: weather element (weatherdata element) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Spécifie les conditions météorologiques d’un emplacement.
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541266"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>weather element (weatherdata element) (Outlook Weather Information Schema)

Spécifie les conditions météorologiques d’un emplacement.
  
## <a name="element-information"></a>Informations sur l’élément

|||
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[weatherdata](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Définit l’élément météo.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[current](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météorologiques actuelles.  <br/> |
|[forecast](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météorologiques futures d’au moins trois jours à l’avance, y compris aujourd’hui : Aujourd’hui, Demain, Jour après Demain.  <br/> |
   
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|attribution  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie la source des informations météorologiques.  <br/> |Valeur du type xs:string  <br/> |
|degreetype  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie l’unité de température de l’emplacement, par exemple, Celsius.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie l’URL de l’image pour l’emplacement.  <br/> |Valeur du type xs:string  <br/> |
|timezone  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie le décalage GMT.  <br/> |Valeur entre -11 et 12 inclus  <br/> |
|url  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie l’URL de la page web du service météo qui contient des informations météorologiques pour l’emplacement spécifié.  <br/> |Valeur du type xs:string  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie le code associé à l’emplacement utilisé pour distinguer plusieurs emplacements qui ont le même nom.  <br/> |Valeur du type xs:string  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie le nom de l’emplacement qui apparaît dans le contrôle de la zone de baisse.  <br/> |Valeur du type xs:string  <br/> |
   

