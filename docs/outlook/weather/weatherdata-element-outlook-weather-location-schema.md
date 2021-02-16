---
title: élément weatherdata (outlook weather location schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Définit l’élément météo.
ms.openlocfilehash: 65dd0ee5686fb773479c8b63a43f51bff67fd2f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540930"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="2130a-103">élément weatherdata (outlook weather location schema)</span><span class="sxs-lookup"><span data-stu-id="2130a-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="2130a-104">Définit l’élément météo.</span><span class="sxs-lookup"><span data-stu-id="2130a-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2130a-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="2130a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2130a-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="2130a-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="2130a-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2130a-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="2130a-108">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="2130a-108">**Schema file**</span></span> <br/> |<span data-ttu-id="2130a-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="2130a-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2130a-110">Définition</span><span class="sxs-lookup"><span data-stu-id="2130a-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2130a-111">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="2130a-111">Elements and attributes</span></span>

<span data-ttu-id="2130a-112">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="2130a-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2130a-113">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2130a-113">Parent elements</span></span>

<span data-ttu-id="2130a-114">Aucune.</span><span class="sxs-lookup"><span data-stu-id="2130a-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2130a-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2130a-115">Child elements</span></span>

|<span data-ttu-id="2130a-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2130a-116">**Element**</span></span>|<span data-ttu-id="2130a-117">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="2130a-117">**Type**</span></span>|<span data-ttu-id="2130a-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="2130a-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2130a-119">météo</span><span class="sxs-lookup"><span data-stu-id="2130a-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="2130a-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="2130a-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="2130a-121">Spécifie l’emplacement où signaler la météo.</span><span class="sxs-lookup"><span data-stu-id="2130a-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2130a-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="2130a-122">Attributes</span></span>

<span data-ttu-id="2130a-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2130a-123">None.</span></span>
  

