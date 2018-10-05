---
title: WeatherData, élément (schéma des informations météo Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Définit l’élément météo.
ms.openlocfilehash: 2273f7ce6c6a04464ea3da430661c3d6f410cc9f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388440"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="4e4bc-103">WeatherData, élément (schéma des informations météo Outlook)</span><span class="sxs-lookup"><span data-stu-id="4e4bc-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="4e4bc-104">Définit l’élément météo.</span><span class="sxs-lookup"><span data-stu-id="4e4bc-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4e4bc-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="4e4bc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e4bc-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="4e4bc-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="4e4bc-107">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="4e4bc-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="4e4bc-108">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4e4bc-108">**Schema file**</span></span> <br/> |<span data-ttu-id="4e4bc-109">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="4e4bc-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4e4bc-110">Définition</span><span class="sxs-lookup"><span data-stu-id="4e4bc-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType">
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4e4bc-111">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4e4bc-111">Elements and attributes</span></span>

<span data-ttu-id="4e4bc-112">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="4e4bc-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4e4bc-113">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4e4bc-113">Parent elements</span></span>

<span data-ttu-id="4e4bc-114">Aucune.</span><span class="sxs-lookup"><span data-stu-id="4e4bc-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e4bc-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4e4bc-115">Child elements</span></span>

|<span data-ttu-id="4e4bc-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4e4bc-116">**Element**</span></span>|<span data-ttu-id="4e4bc-117">**Type**</span><span class="sxs-lookup"><span data-stu-id="4e4bc-117">**Type**</span></span>|<span data-ttu-id="4e4bc-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="4e4bc-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4e4bc-119">météo</span><span class="sxs-lookup"><span data-stu-id="4e4bc-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="4e4bc-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="4e4bc-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="4e4bc-121">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="4e4bc-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4e4bc-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="4e4bc-122">Attributes</span></span>

<span data-ttu-id="4e4bc-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4e4bc-123">None.</span></span>
  

