---
title: Forecast, élément (weatherType complexType) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: "Spécifie les conditions météorologiques futures d'une avance de trois jours, y compris aujourd'hui: aujourd'hui, demain, jour après demain."
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339563"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>Forecast, élément (weatherType complexType) (Outlook Weather Information Schema)

Spécifie les conditions météorologiques futures d'une avance de trois jours, y compris aujourd'hui: aujourd'hui, demain, jour après demain.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |GetWeatherInfo. xsd  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[renseignement](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météorologiques d'un emplacement.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |XS: date  <br/> |obligatoire  <br/> |Indique la date de la prévision.  <br/> |Une valeur de type xs: date  <br/> |
|quotidienne  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie un jour pour la prévision.  <br/> |Une valeur du type xs: String  <br/> |
|important  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Spécifie la température la plus élevée prévue.  <br/> |Valeur de type xs: Integer  <br/> |
|assez  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Spécifie la température minimale prévue.  <br/> |Valeur de type xs: Integer  <br/> |
|PRECIP  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Indique le pourcentage de probabilité de précipitation.  <br/> |Valeur de type xs: Integer  <br/> |
|shortday  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie un jour sous forme abrégée.  <br/> |Une valeur du type xs: String  <br/> |
|skycodeday  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Spécifie un code pour les conditions prévues.  <br/> |Valeur de type xs: Integer  <br/> |
|skytextday  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie un à deux mots qui décrivent les conditions prévues.  <br/> |Une valeur du type xs: String  <br/> |
   

