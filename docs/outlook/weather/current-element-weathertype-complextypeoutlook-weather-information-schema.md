---
title: élément actuel (weatherType complexType) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Spécifie les conditions météorologiques actuelles.
ms.openlocfilehash: ee64fa709bd86fff024d6b6f2ab67f5e9c974971
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64452254"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>élément actuel (weatherType complexType) (Outlook Weather Information Schema)

Spécifie les conditions météorologiques actuelles.
  
## <a name="element-information"></a>Informations sur l'élément

|Propriété |Valeur |
|:-----|:-----|
|**Type d’élément** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="current"      type="currentType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, consultez la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[météo](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météorologiques d’un emplacement. |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |obligatoire  <br/> |Spécifie la date du jour. |Valeur du type xs:date  <br/> |
|day  <br/> |xs:string  <br/> |facultatif  <br/> |Spécifie un jour pour la prévision. |Valeur du type xs:string  <br/> |
|feelslike  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la température de la météo actuelle. |Valeur du type xs:integer  <br/> |
|humidité  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la valeur d’humidité numérique actuelle. |Valeur du type xs:integer  <br/> |
|observationpoint  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie à partir de quel endroit les informations météorologiques actuelles sont observées. |Valeur du type xs:string  <br/> |
|observationtime  <br/> |xs:time  <br/> |obligatoire  <br/> |Indique à quel moment les informations météorologiques actuelles sont observées. |Valeur du type xs:time  <br/> |
|shortday  <br/> |xs:string  <br/> |facultatif  <br/> |Spécifie un jour sous forme abrégée. |Valeur du type xs:string  <br/> |
|skycode  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie un code d’un nombre integer pour les conditions météorologiques actuelles. |Valeur du type xs:integer  <br/> |
|skytext  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un à deux mots décrivant les conditions météorologiques actuelles. |Valeur du type xs:string  <br/> |
|température  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la température actuelle de l’emplacement. |Valeur du type xs:integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |obligatoire  <br/> |Chaîne qui décrit les conditions actuelles du vent. |Valeur du type xs:string  <br/> |
|windspeed  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la valeur actuelle de la vitesse du vent numérique. |Valeur du type xs:integer  <br/> |
   

