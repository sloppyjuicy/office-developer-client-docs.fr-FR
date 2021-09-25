---
title: élément weatherdata (Outlook Weather Location Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Définit l’élément météo.
ms.openlocfilehash: 5c69a0822395668fc1b14263d4ee589ebfb6d16c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603990"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a>élément weatherdata (Outlook Weather Location Schema)

Définit l’élément météo.
  
## <a name="element-information"></a>Informations sur l’élément

|||
|:-----|:-----|
|**Type d’élément** <br/> ||
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Fichier de schéma** <br/> |getweatherlocation.xsd  <br/> |
   
## <a name="definition"></a>Définition

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType" maxOccurs="unbounded"
      >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a>Éléments et attributs

Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition. 
  
### <a name="parent-elements"></a>Éléments parents

Aucune.
  
### <a name="child-elements"></a>Éléments enfants

|**Élément**|**Type (Type)**|**Description**|
|:-----|:-----|:-----|
|[météo](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |Spécifie l’emplacement où signaler la météo.  <br/> |
   
### <a name="attributes"></a>Attributs

Aucun.
  

