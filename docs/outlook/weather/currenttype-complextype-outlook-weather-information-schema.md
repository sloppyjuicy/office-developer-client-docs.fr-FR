---
title: complexType currentType (schéma d'informations météorologiques Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Définit les paramètres relatifs aux conditions météorologiques actuelles d'un emplacement.
ms.openlocfilehash: 16d3e23375f68315c9b9f3a7e914d93f4fec9d0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338450"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>complexType currentType (schéma d'informations météorologiques Outlook)

Définit les paramètres relatifs aux conditions météorologiques actuelles d'un emplacement.
  
## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |GetWeatherInfo. xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
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

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |XS: date  <br/> |obligatoire  <br/> |Indique la date du jour.  <br/> |Une valeur de type xs: date  <br/> |
|quotidienne  <br/> |XS: String  <br/> |facultatif  <br/> |Spécifie un jour pour la prévision.  <br/> |Une valeur du type xs: String  <br/> |
|feelslike  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Indique la température de la météo actuelle.  <br/> |Valeur de type xs: Integer  <br/> |
|Humid  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Indique la valeur d'humidité numérique actuelle.  <br/> |Valeur de type xs: Integer  <br/> |
|observationpoint  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie l'emplacement à partir duquel les informations météorologiques actuelles sont observées.  <br/> |Une valeur du type xs: String  <br/> |
|observationtime  <br/> |XS: Time  <br/> |obligatoire  <br/> |Indique quand les informations météorologiques actuelles sont observées à.  <br/> |Une valeur du type xs: Time  <br/> |
|shortday  <br/> |XS: String  <br/> |facultatif  <br/> |Spécifie un jour sous forme abrégée.  <br/> |Une valeur du type xs: String  <br/> |
|skycode  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Spécifie un code entier pour les conditions météorologiques actuelles.  <br/> |Valeur de type xs: Integer  <br/> |
|skytext  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie un à deux mots qui décrivent les conditions météorologiques actuelles.  <br/> |Une valeur du type xs: String  <br/> |
|régulation  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Indique la température actuelle de l'emplacement.  <br/> |Valeur de type xs: Integer  <br/> |
|winddisplay  <br/> |XS: String  <br/> |obligatoire  <br/> |Chaîne qui décrit les conditions de vent actuelles.  <br/> |Une valeur du type xs: String  <br/> |
|WindSpeed  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Spécifie la valeur numérique de la vitesse du vent.  <br/> |Valeur de type xs: Integer  <br/> |
   

