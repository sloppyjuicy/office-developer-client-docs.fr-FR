---
title: élément WeatherData (schéma d'informations météorologiques Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Définit l'élément météorologique.
ms.openlocfilehash: 2273f7ce6c6a04464ea3da430661c3d6f410cc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355075"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="52460-103">élément WeatherData (schéma d'informations météorologiques Outlook)</span><span class="sxs-lookup"><span data-stu-id="52460-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="52460-104">Définit l'élément météorologique.</span><span class="sxs-lookup"><span data-stu-id="52460-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52460-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="52460-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52460-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="52460-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="52460-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="52460-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="52460-108">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="52460-108">**Schema file**</span></span> <br/> |<span data-ttu-id="52460-109">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="52460-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="52460-110">Définition</span><span class="sxs-lookup"><span data-stu-id="52460-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="52460-111">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="52460-111">Elements and attributes</span></span>

<span data-ttu-id="52460-112">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="52460-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="52460-113">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="52460-113">Parent elements</span></span>

<span data-ttu-id="52460-114">Aucune.</span><span class="sxs-lookup"><span data-stu-id="52460-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52460-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="52460-115">Child elements</span></span>

|<span data-ttu-id="52460-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="52460-116">**Element**</span></span>|<span data-ttu-id="52460-117">**Type**</span><span class="sxs-lookup"><span data-stu-id="52460-117">**Type**</span></span>|<span data-ttu-id="52460-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="52460-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="52460-119">renseignement</span><span class="sxs-lookup"><span data-stu-id="52460-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="52460-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="52460-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="52460-121">Spécifie les conditions météorologiques d'un emplacement.</span><span class="sxs-lookup"><span data-stu-id="52460-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="52460-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="52460-122">Attributes</span></span>

<span data-ttu-id="52460-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="52460-123">None.</span></span>
  

