---
title: type complexe forecastType (schéma des informations météo Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Définit les paramètres sur les conditions de prévisions météorologiques d’un emplacement.
ms.openlocfilehash: 886c6cdbbeb9f07564854dc6a62cbcdad9703b62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787714"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>type complexe forecastType (schéma des informations météo Outlook)

Définit les paramètres sur les conditions de prévisions météorologiques d’un emplacement.
  
## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |GetWeatherInfo.xsd  <br/> |
|**Base d’extension** <br/> |Aucune  <br/> |
   
## <a name="definition"></a>Définition

```XML
       <xs:complexType name="forecastType">
     <xs:attribute name="shortday"   type="xs:string"      use="required"     />
     <xs:attribute name="day"   type="xs:string"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="precip"   type="xs:integer"      use="required"     />
     <xs:attribute name="skytextday"   type="xs:string"      use="required"     />
     <xs:attribute name="skycodeday"   type="xs:integer"      use="required"     />
     <xs:attribute name="high"   type="xs:integer"      use="required"     />
     <xs:attribute name="low"   type="xs:integer"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs : date  <br/> |obligatoire  <br/> |Spécifie la date pour la prévision.  <br/> |Valeur du type xs : date  <br/> |
|jour  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un jour pour la prévision.  <br/> |Valeur du type xs : String  <br/> |
|haute  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la température la plus élevée prévue.  <br/> |Une valeur de la xs : Integer type  <br/> |
|faible  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la température prévue.  <br/> |Une valeur de la xs : Integer type  <br/> |
|precip  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la possibilité de pourcentage de précipitation.  <br/> |Une valeur de la xs : Integer type  <br/> |
|shortday  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un jour sous forme abrégée.  <br/> |Valeur du type xs : String  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie un code pour les conditions prévues.  <br/> |Une valeur de la xs : Integer type  <br/> |
|skytextday  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un ou deux mots qui décrivent les conditions prévues.  <br/> |Valeur du type xs : String  <br/> |
   

