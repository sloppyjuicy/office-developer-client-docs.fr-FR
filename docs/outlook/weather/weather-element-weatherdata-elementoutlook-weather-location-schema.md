---
title: météo élément (weatherdata) (schéma de Outlook météo emplacement)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Spécifie l’emplacement à la météo rapport sur.
ms.openlocfilehash: a95e207845a9e54f5cac58b64ce85ec17b59fa22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787795"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>météo élément (weatherdata) (schéma de Outlook météo emplacement)

Spécifie l’emplacement à la météo rapport sur.
  
## <a name="element-information"></a>Informations sur l'élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**Espace de noms** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Fichier de schéma** <br/> |getweatherlocation.xsd  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[WeatherData](weatherdata-element-outlook-weather-location-schema.md) <br/> ||Définit l’élément météo.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie un code qui est associé à l’emplacement pour distinguer plusieurs emplacements portant le même nom.  <br/> |Valeur du type xs : String  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |obligatoire  <br/> |Spécifie le nom de l’emplacement.  <br/> |Valeur du type xs : String  <br/> |
   

