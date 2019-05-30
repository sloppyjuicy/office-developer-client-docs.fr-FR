---
title: Current, élément (weatherType complexType) (schéma d’informations météorologiques Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Spécifie les conditions météorologiques actuelles.
ms.openlocfilehash: 1303212da1336112599ae5328498cca0d4ab5f89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541007"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>Current, élément (weatherType complexType) (schéma d’informations météorologiques Outlook)

Spécifie les conditions météorologiques actuelles.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |GetWeatherInfo. xsd  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="current"      type="currentType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[renseignement](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météorologiques d’un emplacement.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |XS: date  <br/> |obligatoire  <br/> |Indique la date du jour.  <br/> |Une valeur de type xs: date  <br/> |
|quotidienne  <br/> |XS: String  <br/> |facultatif  <br/> |Spécifie un jour pour la prévision.  <br/> |Une valeur du type xs: String  <br/> |
|feelslike  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Indique la température de la météo actuelle.  <br/> |Valeur de type xs: Integer  <br/> |
|Humid  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Indique la valeur d’humidité numérique actuelle.  <br/> |Valeur de type xs: Integer  <br/> |
|observationpoint  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie l’emplacement à partir duquel les informations météorologiques actuelles sont observées.  <br/> |Une valeur du type xs: String  <br/> |
|observationtime  <br/> |XS: Time  <br/> |obligatoire  <br/> |Indique quand les informations météorologiques actuelles sont observées à.  <br/> |Une valeur du type xs: Time  <br/> |
|shortday  <br/> |XS: String  <br/> |facultatif  <br/> |Spécifie un jour sous forme abrégée.  <br/> |Une valeur du type xs: String  <br/> |
|skycode  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Spécifie un code entier pour les conditions météorologiques actuelles.  <br/> |Valeur de type xs: Integer  <br/> |
|skytext  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie un à deux mots qui décrivent les conditions météorologiques actuelles.  <br/> |Une valeur du type xs: String  <br/> |
|régulation  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Indique la température actuelle de l’emplacement.  <br/> |Valeur de type xs: Integer  <br/> |
|winddisplay  <br/> |XS: String  <br/> |obligatoire  <br/> |Chaîne qui décrit les conditions de vent actuelles.  <br/> |Une valeur du type xs: String  <br/> |
|windspeed  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Spécifie la valeur numérique de la vitesse du vent.  <br/> |Valeur de type xs: Integer  <br/> |
   

