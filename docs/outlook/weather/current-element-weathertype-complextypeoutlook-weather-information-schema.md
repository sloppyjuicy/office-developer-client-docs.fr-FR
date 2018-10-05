---
title: élément en cours (weatherType, complexType) (schéma des informations météo Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Spécifie la météo.
ms.openlocfilehash: ce92bdd49ee37f939748586c2d63d8a664f664d2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401089"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>élément en cours (weatherType, complexType) (schéma des informations météo Outlook)

Spécifie la météo.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="current"      type="currentType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[météo](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Spécifie les conditions météorologiques d’un emplacement.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs : date  <br/> |obligatoire  <br/> |Spécifie la date du jour.  <br/> |Valeur du type xs : date  <br/> |
|jour  <br/> |xs:string  <br/> |facultatif  <br/> |Spécifie un jour pour la prévision.  <br/> |Valeur du type xs : String  <br/> |
|feelslike  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie comment la météo actuelle semble la température.  <br/> |Une valeur de la xs : Integer type  <br/> |
|humidité  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la valeur numérique humidité actuel.  <br/> |Une valeur de la xs : Integer type  <br/> |
|observationpoint  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie où la météo actuelle est observée à partir.  <br/> |Valeur du type xs : String  <br/> |
|observationtime  <br/> |xs : Time  <br/> |obligatoire  <br/> |Spécifie que lorsque la météo actuelle est observée à.  <br/> |Une valeur de la xs : time type  <br/> |
|shortday  <br/> |xs:string  <br/> |facultatif  <br/> |Spécifie un jour sous forme abrégée.  <br/> |Valeur du type xs : String  <br/> |
|skycode  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie un code de type entier pour la météo.  <br/> |Une valeur de la xs : Integer type  <br/> |
|skytext  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un ou deux mots décrivant la météo.  <br/> |Valeur du type xs : String  <br/> |
|température  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la température de l’emplacement actuelle.  <br/> |Une valeur de la xs : Integer type  <br/> |
|winddisplay  <br/> |xs:string  <br/> |obligatoire  <br/> |Chaîne qui décrit les conditions de vent en cours.  <br/> |Valeur du type xs : String  <br/> |
|vitesse du vent  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la valeur actuelle de la vitesse vent numérique.  <br/> |Une valeur de la xs : Integer type  <br/> |
   

