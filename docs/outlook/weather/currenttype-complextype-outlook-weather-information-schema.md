---
title: currentType complexType (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Définit les paramètres sur les conditions météorologiques actuelles d’un emplacement.
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540986"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>currentType complexType (Outlook Weather Information Schema)

Définit les paramètres sur les conditions météorologiques actuelles d’un emplacement.
  
## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |getweatherinfo.xsd  <br/> |
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |obligatoire  <br/> |Spécifie la date du jour.  <br/> |Valeur du type xs:date  <br/> |
|day  <br/> |xs:string  <br/> |facultatif  <br/> |Spécifie un jour pour la prévision.  <br/> |Valeur du type xs:string  <br/> |
|feelslike  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la température de la météo actuelle.  <br/> |Valeur du type xs:integer  <br/> |
|humidité  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la valeur d’humidité numérique actuelle.  <br/> |Valeur du type xs:integer  <br/> |
|observationpoint  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie à partir de quel endroit les informations météorologiques actuelles sont observées.  <br/> |Valeur du type xs:string  <br/> |
|observationtime  <br/> |xs:time  <br/> |obligatoire  <br/> |Indique à quel moment les informations météorologiques actuelles sont observées.  <br/> |Valeur du type xs:time  <br/> |
|shortday  <br/> |xs:string  <br/> |facultatif  <br/> |Spécifie un jour sous forme abrégée.  <br/> |Valeur du type xs:string  <br/> |
|skycode  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie un code d’un nombre integer pour les conditions météorologiques actuelles.  <br/> |Valeur du type xs:integer  <br/> |
|skytext  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un à deux mots décrivant les conditions météorologiques actuelles.  <br/> |Valeur du type xs:string  <br/> |
|température  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la température actuelle de l’emplacement.  <br/> |Valeur du type xs:integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |obligatoire  <br/> |Chaîne qui décrit les conditions actuelles du vent.  <br/> |Valeur du type xs:string  <br/> |
|windspeed  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la valeur actuelle de la vitesse du vent numérique.  <br/> |Valeur du type xs:integer  <br/> |
   

