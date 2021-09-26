---
title: forecastType complexType (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Définit les paramètres des prévisions météorologiques d’un emplacement.
ms.openlocfilehash: 815f7131fc4869a7015c0fee15d0e8d68d0905dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619315"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (Outlook Weather Information Schema)

Définit les paramètres des prévisions météorologiques d’un emplacement.
  
## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |getweatherinfo.xsd  <br/> |
|**Base d’extension** <br/> |Aucun  <br/> |
   
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

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |obligatoire  <br/> |Spécifie la date de la prévision.  <br/> |Valeur du type xs:date  <br/> |
|day  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un jour pour la prévision.  <br/> |Valeur du type xs:string  <br/> |
|high  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la température la plus élevée prévue.  <br/> |Valeur du type xs:integer  <br/> |
|faible  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la température la plus basse prévue.  <br/> |Valeur du type xs:integer  <br/> |
|precip  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie la possibilité de pourcentage d’éventualité.  <br/> |Valeur du type xs:integer  <br/> |
|shortday  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un jour sous forme abrégée.  <br/> |Valeur du type xs:string  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |obligatoire  <br/> |Spécifie un code pour les conditions prévues.  <br/> |Valeur du type xs:integer  <br/> |
|skytextday  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un à deux mots qui décrivent les conditions prévues.  <br/> |Valeur du type xs:string  <br/> |
   

