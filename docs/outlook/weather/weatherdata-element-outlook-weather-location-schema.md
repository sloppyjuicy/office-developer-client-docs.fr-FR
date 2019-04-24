---
title: élément WeatherData (schéma d'emplacement météorologique Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Définit l'élément météorologique.
ms.openlocfilehash: ade57264fab592d3314aa9a3376e129a5f3719c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355033"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="03101-103">élément WeatherData (schéma d'emplacement météorologique Outlook)</span><span class="sxs-lookup"><span data-stu-id="03101-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="03101-104">Définit l'élément météorologique.</span><span class="sxs-lookup"><span data-stu-id="03101-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="03101-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="03101-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03101-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="03101-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="03101-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="03101-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="03101-108">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="03101-108">**Schema file**</span></span> <br/> |<span data-ttu-id="03101-109">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="03101-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="03101-110">Définition</span><span class="sxs-lookup"><span data-stu-id="03101-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="03101-111">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="03101-111">Elements and attributes</span></span>

<span data-ttu-id="03101-112">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="03101-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="03101-113">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="03101-113">Parent elements</span></span>

<span data-ttu-id="03101-114">Aucune.</span><span class="sxs-lookup"><span data-stu-id="03101-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="03101-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="03101-115">Child elements</span></span>

|<span data-ttu-id="03101-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="03101-116">**Element**</span></span>|<span data-ttu-id="03101-117">**Type**</span><span class="sxs-lookup"><span data-stu-id="03101-117">**Type**</span></span>|<span data-ttu-id="03101-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="03101-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="03101-119">renseignement</span><span class="sxs-lookup"><span data-stu-id="03101-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="03101-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="03101-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="03101-121">Spécifie l'emplacement de la météo.</span><span class="sxs-lookup"><span data-stu-id="03101-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="03101-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="03101-122">Attributes</span></span>

<span data-ttu-id="03101-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="03101-123">None.</span></span>
  

