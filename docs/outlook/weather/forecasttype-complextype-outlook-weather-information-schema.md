---
title: complexType forecastType (schéma d’informations météorologiques Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Définit les paramètres relatifs aux conditions météorologiques de prévision d’un emplacement.
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540951"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>complexType forecastType (schéma d’informations météorologiques Outlook)

Définit les paramètres relatifs aux conditions météorologiques de prévision d’un emplacement.
  
## <a name="type-information"></a>Informations sur le type

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Fichier de schéma** <br/> |GetWeatherInfo. xsd  <br/> |
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

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |XS: date  <br/> |obligatoire  <br/> |Indique la date de la prévision.  <br/> |Une valeur de type xs: date  <br/> |
|quotidienne  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie un jour pour la prévision.  <br/> |Une valeur du type xs: String  <br/> |
|important  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Spécifie la température la plus élevée prévue.  <br/> |Valeur de type xs: Integer  <br/> |
|assez  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Spécifie la température minimale prévue.  <br/> |Valeur de type xs: Integer  <br/> |
|precip  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Indique le pourcentage de probabilité de précipitation.  <br/> |Valeur de type xs: Integer  <br/> |
|shortday  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie un jour sous forme abrégée.  <br/> |Une valeur du type xs: String  <br/> |
|skycodeday  <br/> |XS: Integer  <br/> |obligatoire  <br/> |Spécifie un code pour les conditions prévues.  <br/> |Valeur de type xs: Integer  <br/> |
|skytextday  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie un à deux mots qui décrivent les conditions prévues.  <br/> |Une valeur du type xs: String  <br/> |
   

