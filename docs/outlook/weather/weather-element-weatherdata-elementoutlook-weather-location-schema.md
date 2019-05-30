---
title: élément météorologique (élément WeatherData) (schéma d’emplacement météorologique Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Spécifie l’emplacement de la météo.
ms.openlocfilehash: a907fb9df02d88d317a73e409ea8738273eb2cb1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539011"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="1207c-103">élément météorologique (élément WeatherData) (schéma d’emplacement météorologique Outlook)</span><span class="sxs-lookup"><span data-stu-id="1207c-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="1207c-104">Spécifie l’emplacement de la météo.</span><span class="sxs-lookup"><span data-stu-id="1207c-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1207c-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="1207c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1207c-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="1207c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1207c-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="1207c-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="1207c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1207c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="1207c-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1207c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1207c-110">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="1207c-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1207c-111">Définition</span><span class="sxs-lookup"><span data-stu-id="1207c-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="1207c-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1207c-112">Elements and attributes</span></span>

<span data-ttu-id="1207c-113">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="1207c-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1207c-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1207c-114">Parent elements</span></span>

|<span data-ttu-id="1207c-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1207c-115">**Element**</span></span>|<span data-ttu-id="1207c-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="1207c-116">**Type**</span></span>|<span data-ttu-id="1207c-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="1207c-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1207c-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="1207c-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="1207c-119">Définit l’élément météorologique.</span><span class="sxs-lookup"><span data-stu-id="1207c-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1207c-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1207c-120">Child elements</span></span>

<span data-ttu-id="1207c-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1207c-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1207c-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="1207c-122">Attributes</span></span>

|<span data-ttu-id="1207c-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1207c-123">**Attribute**</span></span>|<span data-ttu-id="1207c-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="1207c-124">**Type**</span></span>|<span data-ttu-id="1207c-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="1207c-125">**Required**</span></span>|<span data-ttu-id="1207c-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="1207c-126">**Description**</span></span>|<span data-ttu-id="1207c-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="1207c-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1207c-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="1207c-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="1207c-129">XS: String</span><span class="sxs-lookup"><span data-stu-id="1207c-129">xs:string</span></span>  <br/> |<span data-ttu-id="1207c-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1207c-130">required</span></span>  <br/> |<span data-ttu-id="1207c-131">Spécifie un code associé à l’emplacement pour distinguer plusieurs emplacements portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="1207c-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="1207c-132">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="1207c-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="1207c-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="1207c-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="1207c-134">XS: String</span><span class="sxs-lookup"><span data-stu-id="1207c-134">xs:string</span></span>  <br/> |<span data-ttu-id="1207c-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1207c-135">required</span></span>  <br/> |<span data-ttu-id="1207c-136">Spécifie le nom de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="1207c-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="1207c-137">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="1207c-137">A value of the type xs:string</span></span>  <br/> |
   

