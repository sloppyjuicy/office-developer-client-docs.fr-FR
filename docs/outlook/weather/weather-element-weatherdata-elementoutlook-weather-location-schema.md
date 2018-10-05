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
ms.openlocfilehash: f6642b3f477b9fe45ed0e6a43efcd40e21559b7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398296"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="c35f2-103">météo élément (weatherdata) (schéma de Outlook météo emplacement)</span><span class="sxs-lookup"><span data-stu-id="c35f2-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="c35f2-104">Spécifie l’emplacement à la météo rapport sur.</span><span class="sxs-lookup"><span data-stu-id="c35f2-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c35f2-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="c35f2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c35f2-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="c35f2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c35f2-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="c35f2-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="c35f2-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c35f2-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="c35f2-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c35f2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c35f2-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="c35f2-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c35f2-111">Définition</span><span class="sxs-lookup"><span data-stu-id="c35f2-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="c35f2-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c35f2-112">Elements and attributes</span></span>

<span data-ttu-id="c35f2-113">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c35f2-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c35f2-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c35f2-114">Parent elements</span></span>

|<span data-ttu-id="c35f2-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c35f2-115">**Element**</span></span>|<span data-ttu-id="c35f2-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="c35f2-116">**Type**</span></span>|<span data-ttu-id="c35f2-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="c35f2-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c35f2-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="c35f2-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="c35f2-119">Définit l’élément météo.</span><span class="sxs-lookup"><span data-stu-id="c35f2-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c35f2-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c35f2-120">Child elements</span></span>

<span data-ttu-id="c35f2-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c35f2-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c35f2-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="c35f2-122">Attributes</span></span>

|<span data-ttu-id="c35f2-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c35f2-123">**Attribute**</span></span>|<span data-ttu-id="c35f2-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="c35f2-124">**Type**</span></span>|<span data-ttu-id="c35f2-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c35f2-125">**Required**</span></span>|<span data-ttu-id="c35f2-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="c35f2-126">**Description**</span></span>|<span data-ttu-id="c35f2-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c35f2-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c35f2-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="c35f2-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="c35f2-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="c35f2-129">xs:string</span></span>  <br/> |<span data-ttu-id="c35f2-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c35f2-130">required</span></span>  <br/> |<span data-ttu-id="c35f2-131">Spécifie un code qui est associé à l’emplacement pour distinguer plusieurs emplacements portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="c35f2-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="c35f2-132">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="c35f2-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="c35f2-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="c35f2-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="c35f2-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="c35f2-134">xs:string</span></span>  <br/> |<span data-ttu-id="c35f2-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c35f2-135">required</span></span>  <br/> |<span data-ttu-id="c35f2-136">Spécifie le nom de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="c35f2-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="c35f2-137">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="c35f2-137">A value of the type xs:string</span></span>  <br/> |
   

