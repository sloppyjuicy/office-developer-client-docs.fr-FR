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
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="365f7-103">météo élément (weatherdata) (schéma de Outlook météo emplacement)</span><span class="sxs-lookup"><span data-stu-id="365f7-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="365f7-104">Spécifie l’emplacement à la météo rapport sur.</span><span class="sxs-lookup"><span data-stu-id="365f7-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="365f7-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="365f7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="365f7-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="365f7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="365f7-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="365f7-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="365f7-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="365f7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="365f7-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="365f7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="365f7-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="365f7-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="365f7-111">Définition</span><span class="sxs-lookup"><span data-stu-id="365f7-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="365f7-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="365f7-112">Elements and attributes</span></span>

<span data-ttu-id="365f7-113">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="365f7-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="365f7-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="365f7-114">Parent elements</span></span>

|<span data-ttu-id="365f7-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="365f7-115">**Element**</span></span>|<span data-ttu-id="365f7-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="365f7-116">**Type**</span></span>|<span data-ttu-id="365f7-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="365f7-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="365f7-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="365f7-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="365f7-119">Définit l’élément météo.</span><span class="sxs-lookup"><span data-stu-id="365f7-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="365f7-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="365f7-120">Child elements</span></span>

<span data-ttu-id="365f7-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="365f7-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="365f7-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="365f7-122">Attributes</span></span>

|<span data-ttu-id="365f7-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="365f7-123">**Attribute**</span></span>|<span data-ttu-id="365f7-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="365f7-124">**Type**</span></span>|<span data-ttu-id="365f7-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="365f7-125">**Required**</span></span>|<span data-ttu-id="365f7-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="365f7-126">**Description**</span></span>|<span data-ttu-id="365f7-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="365f7-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="365f7-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="365f7-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="365f7-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="365f7-129">xs:string</span></span>  <br/> |<span data-ttu-id="365f7-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="365f7-130">required</span></span>  <br/> |<span data-ttu-id="365f7-131">Spécifie un code qui est associé à l’emplacement pour distinguer plusieurs emplacements portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="365f7-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="365f7-132">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="365f7-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="365f7-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="365f7-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="365f7-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="365f7-134">xs:string</span></span>  <br/> |<span data-ttu-id="365f7-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="365f7-135">required</span></span>  <br/> |<span data-ttu-id="365f7-136">Spécifie le nom de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="365f7-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="365f7-137">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="365f7-137">A value of the type xs:string</span></span>  <br/> |
   

