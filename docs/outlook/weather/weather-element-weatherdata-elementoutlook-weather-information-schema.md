---
title: Weather, élément (élément WeatherData) (schéma météo Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Spécifie les conditions météorologiques d’un emplacement.
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541266"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="ede5b-103">Weather, élément (élément WeatherData) (schéma météo Outlook)</span><span class="sxs-lookup"><span data-stu-id="ede5b-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="ede5b-104">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="ede5b-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ede5b-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="ede5b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ede5b-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ede5b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ede5b-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="ede5b-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="ede5b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ede5b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="ede5b-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ede5b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ede5b-110">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="ede5b-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ede5b-111">Définition</span><span class="sxs-lookup"><span data-stu-id="ede5b-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="ede5b-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ede5b-112">Elements and attributes</span></span>

<span data-ttu-id="ede5b-113">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="ede5b-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ede5b-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ede5b-114">Parent elements</span></span>

|<span data-ttu-id="ede5b-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ede5b-115">**Element**</span></span>|<span data-ttu-id="ede5b-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="ede5b-116">**Type**</span></span>|<span data-ttu-id="ede5b-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="ede5b-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ede5b-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="ede5b-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="ede5b-119">Définit l’élément météorologique.</span><span class="sxs-lookup"><span data-stu-id="ede5b-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ede5b-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ede5b-120">Child elements</span></span>

|<span data-ttu-id="ede5b-121">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ede5b-121">**Element**</span></span>|<span data-ttu-id="ede5b-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="ede5b-122">**Type**</span></span>|<span data-ttu-id="ede5b-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="ede5b-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ede5b-124">récent</span><span class="sxs-lookup"><span data-stu-id="ede5b-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="ede5b-125">currentType</span><span class="sxs-lookup"><span data-stu-id="ede5b-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="ede5b-126">Spécifie les conditions météorologiques actuelles.</span><span class="sxs-lookup"><span data-stu-id="ede5b-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="ede5b-127">prévisionnel</span><span class="sxs-lookup"><span data-stu-id="ede5b-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="ede5b-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="ede5b-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="ede5b-129">Spécifie les conditions météorologiques futures d’une avance de trois jours, y compris aujourd’hui: aujourd’hui, demain, jour après demain.</span><span class="sxs-lookup"><span data-stu-id="ede5b-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ede5b-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="ede5b-130">Attributes</span></span>

|<span data-ttu-id="ede5b-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ede5b-131">**Attribute**</span></span>|<span data-ttu-id="ede5b-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="ede5b-132">**Type**</span></span>|<span data-ttu-id="ede5b-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ede5b-133">**Required**</span></span>|<span data-ttu-id="ede5b-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="ede5b-134">**Description**</span></span>|<span data-ttu-id="ede5b-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ede5b-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ede5b-136">attribution</span><span class="sxs-lookup"><span data-stu-id="ede5b-136">attribution</span></span>  <br/> |<span data-ttu-id="ede5b-137">XS: String</span><span class="sxs-lookup"><span data-stu-id="ede5b-137">xs:string</span></span>  <br/> |<span data-ttu-id="ede5b-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ede5b-138">required</span></span>  <br/> |<span data-ttu-id="ede5b-139">Spécifie la source des informations météorologiques.</span><span class="sxs-lookup"><span data-stu-id="ede5b-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="ede5b-140">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="ede5b-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ede5b-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="ede5b-141">degreetype</span></span>  <br/> |<span data-ttu-id="ede5b-142">XS: String</span><span class="sxs-lookup"><span data-stu-id="ede5b-142">xs:string</span></span>  <br/> |<span data-ttu-id="ede5b-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ede5b-143">required</span></span>  <br/> |<span data-ttu-id="ede5b-144">Indique l’unité de température de l’emplacement (par exemple, Celsius).</span><span class="sxs-lookup"><span data-stu-id="ede5b-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="ede5b-145">C, F</span><span class="sxs-lookup"><span data-stu-id="ede5b-145">C, F</span></span>  <br/> |
|<span data-ttu-id="ede5b-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="ede5b-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="ede5b-147">XS: String</span><span class="sxs-lookup"><span data-stu-id="ede5b-147">xs:string</span></span>  <br/> |<span data-ttu-id="ede5b-148">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ede5b-148">required</span></span>  <br/> |<span data-ttu-id="ede5b-149">Spécifie l’URL de l’image pour l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="ede5b-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="ede5b-150">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="ede5b-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ede5b-151">horaire</span><span class="sxs-lookup"><span data-stu-id="ede5b-151">timezone</span></span>  <br/> |<span data-ttu-id="ede5b-152">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="ede5b-152">xs:integer</span></span>  <br/> |<span data-ttu-id="ede5b-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ede5b-153">required</span></span>  <br/> |<span data-ttu-id="ede5b-154">Spécifie le décalage GMT.</span><span class="sxs-lookup"><span data-stu-id="ede5b-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="ede5b-155">Une valeur comprise entre-11 et 12 inclus</span><span class="sxs-lookup"><span data-stu-id="ede5b-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="ede5b-156">url</span><span class="sxs-lookup"><span data-stu-id="ede5b-156">url</span></span>  <br/> |<span data-ttu-id="ede5b-157">XS: String</span><span class="sxs-lookup"><span data-stu-id="ede5b-157">xs:string</span></span>  <br/> |<span data-ttu-id="ede5b-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ede5b-158">required</span></span>  <br/> |<span data-ttu-id="ede5b-159">Spécifie l’URL de la page Web du service météo qui contient des informations météorologiques pour l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="ede5b-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="ede5b-160">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="ede5b-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ede5b-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="ede5b-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="ede5b-162">XS: String</span><span class="sxs-lookup"><span data-stu-id="ede5b-162">xs:string</span></span>  <br/> |<span data-ttu-id="ede5b-163">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ede5b-163">required</span></span>  <br/> |<span data-ttu-id="ede5b-164">Spécifie le code associé à l’emplacement utilisé pour distinguer plusieurs emplacements portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="ede5b-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="ede5b-165">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="ede5b-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ede5b-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="ede5b-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="ede5b-167">XS: String</span><span class="sxs-lookup"><span data-stu-id="ede5b-167">xs:string</span></span>  <br/> |<span data-ttu-id="ede5b-168">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ede5b-168">required</span></span>  <br/> |<span data-ttu-id="ede5b-169">Spécifie le nom de l’emplacement qui apparaît dans le contrôle de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="ede5b-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="ede5b-170">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="ede5b-170">A value of the type xs:string</span></span>  <br/> |
   

