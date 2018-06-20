---
title: WeatherData, élément (schéma de Outlook météo emplacement)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Définit l’élément météo.
ms.openlocfilehash: 5a3d0ed0fbf8d06472a6d9af727a41d97c0231cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787821"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="c5310-103">WeatherData, élément (schéma de Outlook météo emplacement)</span><span class="sxs-lookup"><span data-stu-id="c5310-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="c5310-104">Définit l’élément météo.</span><span class="sxs-lookup"><span data-stu-id="c5310-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5310-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="c5310-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5310-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="c5310-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="c5310-107">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c5310-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="c5310-108">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c5310-108">**Schema file**</span></span> <br/> |<span data-ttu-id="c5310-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="c5310-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c5310-110">Définition</span><span class="sxs-lookup"><span data-stu-id="c5310-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c5310-111">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c5310-111">Elements and attributes</span></span>

<span data-ttu-id="c5310-112">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c5310-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c5310-113">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c5310-113">Parent elements</span></span>

<span data-ttu-id="c5310-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c5310-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5310-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c5310-115">Child elements</span></span>

|<span data-ttu-id="c5310-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c5310-116">**Element**</span></span>|<span data-ttu-id="c5310-117">**Type**</span><span class="sxs-lookup"><span data-stu-id="c5310-117">**Type**</span></span>|<span data-ttu-id="c5310-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="c5310-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c5310-119">météo</span><span class="sxs-lookup"><span data-stu-id="c5310-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="c5310-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="c5310-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="c5310-121">Spécifie l’emplacement à la météo rapport sur.</span><span class="sxs-lookup"><span data-stu-id="c5310-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c5310-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="c5310-122">Attributes</span></span>

<span data-ttu-id="c5310-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c5310-123">None.</span></span>
  

