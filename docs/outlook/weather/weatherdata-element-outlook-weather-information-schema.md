---
title: élément WeatherData (schéma d’informations météorologiques Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Définit l’élément météorologique.
ms.openlocfilehash: bb8c76efd03661083a15aa315cf42c3a6c088b6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538983"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="fc557-103">élément WeatherData (schéma d’informations météorologiques Outlook)</span><span class="sxs-lookup"><span data-stu-id="fc557-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="fc557-104">Définit l’élément météorologique.</span><span class="sxs-lookup"><span data-stu-id="fc557-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc557-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="fc557-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc557-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="fc557-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="fc557-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fc557-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="fc557-108">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fc557-108">**Schema file**</span></span> <br/> |<span data-ttu-id="fc557-109">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="fc557-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fc557-110">Définition</span><span class="sxs-lookup"><span data-stu-id="fc557-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="fc557-111">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fc557-111">Elements and attributes</span></span>

<span data-ttu-id="fc557-112">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="fc557-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fc557-113">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fc557-113">Parent elements</span></span>

<span data-ttu-id="fc557-114">Aucune.</span><span class="sxs-lookup"><span data-stu-id="fc557-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc557-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fc557-115">Child elements</span></span>

|<span data-ttu-id="fc557-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fc557-116">**Element**</span></span>|<span data-ttu-id="fc557-117">**Type**</span><span class="sxs-lookup"><span data-stu-id="fc557-117">**Type**</span></span>|<span data-ttu-id="fc557-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="fc557-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc557-119">renseignement</span><span class="sxs-lookup"><span data-stu-id="fc557-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="fc557-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="fc557-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="fc557-121">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="fc557-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fc557-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="fc557-122">Attributes</span></span>

<span data-ttu-id="fc557-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fc557-123">None.</span></span>
  

