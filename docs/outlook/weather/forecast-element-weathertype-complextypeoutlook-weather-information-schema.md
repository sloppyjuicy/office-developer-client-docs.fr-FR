---
title: forecast, élément (weatherType complexType) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Spécifie les conditions météorologiques futures d’au moins trois jours à l’avance, y compris aujourd’hui : Aujourd’hui, Demain, Jour après Demain.'
ms.openlocfilehash: bab9849c797e35b21013c20b09d980bf4d1fd6ac
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406210"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>forecast, élément (weatherType complexType) (Outlook Weather Information Schema)

Spécifie les conditions météorologiques futures d’au moins trois jours à l’avance, y compris aujourd’hui : Aujourd’hui, Demain, Jour après Demain.
  
## <a name="element-information"></a>Informations sur l'élément

||Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[météo](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météorologiques d’un emplacement. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |obligatoire  <br/> |Spécifie la date de la prévision. |Valeur du type xs:date  <br/> |
|day  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un jour pour la prévision. |Valeur du type xs:string  <br/> |
|high  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la température la plus élevée prévue. |Valeur du type xs:integer  <br/> |
|low  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la température la plus basse prévue. |Valeur du type xs:integer  <br/> |
|precip  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la possibilité de pourcentage d’éventualité. |Valeur du type xs:integer  <br/> |
|shortday  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un jour sous forme abrégée. |Valeur du type xs:string  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie un code pour les conditions prévues. |Valeur du type xs:integer  <br/> |
|skytextday  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un à deux mots qui décrivent les conditions prévues. |Valeur du type xs:string  <br/> |
   

