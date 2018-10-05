---
title: type complexe currentType (schéma des informations météo Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Définit les paramètres sur la météo d’un emplacement.
ms.openlocfilehash: 16d3e23375f68315c9b9f3a7e914d93f4fec9d0a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387033"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>type complexe currentType (schéma des informations météo Outlook)

Définit les paramètres sur la météo d’un emplacement.
  
## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Espace de noms** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |GetWeatherInfo.xsd  <br/> |
|**Base d’extension** <br/> |Aucune  <br/> |
   
## <a name="definition"></a>Définition

```XML
       <xs:complexType name="currentType">
     <xs:attribute name="winddisplay"   type="xs:string"      use="required"     />
     <xs:attribute name="windspeed"   type="xs:integer"      use="required"     />
     <xs:attribute name="humidity"   type="xs:integer"      use="required"     />
     <xs:attribute name="feelslike"   type="xs:integer"      use="required"     />
     <xs:attribute name="observationpoint"   type="xs:string"      use="required"     />
     <xs:attribute name="observationtime"   type="xs:time"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="skytext"   type="xs:string"      use="required"     />
     <xs:attribute name="skycode"   type="xs:integer"      use="required"     />
     <xs:attribute name="temperature"   type="xs:integer"      use="required"     />
     <xs:attribute name="shortday"   type="xs:string"      use="optional"     />
     <xs:attribute name="day"   type="xs:string"      use="optional"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
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
   

