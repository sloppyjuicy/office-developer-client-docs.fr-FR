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
ms.openlocfilehash: ade57264fab592d3314aa9a3376e129a5f3719c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391310"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="77a6d-103">WeatherData, élément (schéma de Outlook météo emplacement)</span><span class="sxs-lookup"><span data-stu-id="77a6d-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="77a6d-104">Définit l’élément météo.</span><span class="sxs-lookup"><span data-stu-id="77a6d-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77a6d-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="77a6d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77a6d-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="77a6d-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="77a6d-107">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="77a6d-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="77a6d-108">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="77a6d-108">**Schema file**</span></span> <br/> |<span data-ttu-id="77a6d-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="77a6d-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="77a6d-110">Définition</span><span class="sxs-lookup"><span data-stu-id="77a6d-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="77a6d-111">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="77a6d-111">Elements and attributes</span></span>

<span data-ttu-id="77a6d-112">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="77a6d-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="77a6d-113">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="77a6d-113">Parent elements</span></span>

<span data-ttu-id="77a6d-114">Aucune.</span><span class="sxs-lookup"><span data-stu-id="77a6d-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77a6d-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="77a6d-115">Child elements</span></span>

|<span data-ttu-id="77a6d-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="77a6d-116">**Element**</span></span>|<span data-ttu-id="77a6d-117">**Type**</span><span class="sxs-lookup"><span data-stu-id="77a6d-117">**Type**</span></span>|<span data-ttu-id="77a6d-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="77a6d-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="77a6d-119">météo</span><span class="sxs-lookup"><span data-stu-id="77a6d-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="77a6d-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="77a6d-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="77a6d-121">Spécifie l’emplacement à la météo rapport sur.</span><span class="sxs-lookup"><span data-stu-id="77a6d-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="77a6d-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="77a6d-122">Attributes</span></span>

<span data-ttu-id="77a6d-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="77a6d-123">None.</span></span>
  

