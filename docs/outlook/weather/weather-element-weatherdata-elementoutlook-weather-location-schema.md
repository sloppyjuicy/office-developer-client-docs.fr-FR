---
title: élément météorologique (élément WeatherData) (schéma d'emplacement météorologique Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Spécifie l'emplacement de la météo.
ms.openlocfilehash: f6642b3f477b9fe45ed0e6a43efcd40e21559b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355208"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>élément météorologique (élément WeatherData) (schéma d'emplacement météorologique Outlook)

Spécifie l'emplacement de la météo.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Fichier de schéma** <br/> |getweatherlocation. xsd  <br/> |
   
## <a name="definition"></a>Définition

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition. 
  
### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Type**|**Description**|
|:-----|:-----|:-----|
|[WeatherData](weatherdata-element-outlook-weather-location-schema.md) <br/> ||Définit l'élément météorologique.  <br/> |
   
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="attributes"></a>Attributs

|**Attribut**|**Type**|**Obligatoire**|**Description**|**Valeurs possibles**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie un code associé à l'emplacement pour distinguer plusieurs emplacements portant le même nom.  <br/> |Une valeur du type xs: String  <br/> |
|weatherlocationname  <br/> |XS: String  <br/> |obligatoire  <br/> |Spécifie le nom de l'emplacement.  <br/> |Une valeur du type xs: String  <br/> |
   

