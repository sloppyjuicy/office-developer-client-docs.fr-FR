---
title: météo élément (weatherdata) (schéma des informations météo Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Spécifie les conditions météorologiques d’un emplacement.
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390659"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="4c88d-103">météo élément (weatherdata) (schéma des informations météo Outlook)</span><span class="sxs-lookup"><span data-stu-id="4c88d-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="4c88d-104">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="4c88d-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c88d-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="4c88d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c88d-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="4c88d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4c88d-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="4c88d-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="4c88d-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="4c88d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="4c88d-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4c88d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4c88d-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="4c88d-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4c88d-111">Définition</span><span class="sxs-lookup"><span data-stu-id="4c88d-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="4c88d-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4c88d-112">Elements and attributes</span></span>

<span data-ttu-id="4c88d-113">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="4c88d-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4c88d-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4c88d-114">Parent elements</span></span>

|<span data-ttu-id="4c88d-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4c88d-115">**Element**</span></span>|<span data-ttu-id="4c88d-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="4c88d-116">**Type**</span></span>|<span data-ttu-id="4c88d-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="4c88d-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4c88d-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="4c88d-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="4c88d-119">Définit l’élément météo.</span><span class="sxs-lookup"><span data-stu-id="4c88d-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4c88d-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4c88d-120">Child elements</span></span>

|<span data-ttu-id="4c88d-121">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4c88d-121">**Element**</span></span>|<span data-ttu-id="4c88d-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="4c88d-122">**Type**</span></span>|<span data-ttu-id="4c88d-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="4c88d-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4c88d-124">en cours</span><span class="sxs-lookup"><span data-stu-id="4c88d-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="4c88d-125">currentType</span><span class="sxs-lookup"><span data-stu-id="4c88d-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="4c88d-126">Spécifie la météo.</span><span class="sxs-lookup"><span data-stu-id="4c88d-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="4c88d-127">prévision</span><span class="sxs-lookup"><span data-stu-id="4c88d-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="4c88d-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="4c88d-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="4c88d-129">Spécifie les conditions météo future d’au moins trois jours avance y compris aujourd'hui : aujourd'hui, demain, jour après demain.</span><span class="sxs-lookup"><span data-stu-id="4c88d-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4c88d-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="4c88d-130">Attributes</span></span>

|<span data-ttu-id="4c88d-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4c88d-131">**Attribute**</span></span>|<span data-ttu-id="4c88d-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="4c88d-132">**Type**</span></span>|<span data-ttu-id="4c88d-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4c88d-133">**Required**</span></span>|<span data-ttu-id="4c88d-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="4c88d-134">**Description**</span></span>|<span data-ttu-id="4c88d-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4c88d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4c88d-136">attribution</span><span class="sxs-lookup"><span data-stu-id="4c88d-136">attribution</span></span>  <br/> |<span data-ttu-id="4c88d-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="4c88d-137">xs:string</span></span>  <br/> |<span data-ttu-id="4c88d-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4c88d-138">required</span></span>  <br/> |<span data-ttu-id="4c88d-139">Spécifie la source de la météo.</span><span class="sxs-lookup"><span data-stu-id="4c88d-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="4c88d-140">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="4c88d-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4c88d-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="4c88d-141">degreetype</span></span>  <br/> |<span data-ttu-id="4c88d-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="4c88d-142">xs:string</span></span>  <br/> |<span data-ttu-id="4c88d-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4c88d-143">required</span></span>  <br/> |<span data-ttu-id="4c88d-144">Spécifie l’unité de la température de l’emplacement, par exemple, Celsius.</span><span class="sxs-lookup"><span data-stu-id="4c88d-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="4c88d-145">C, F</span><span class="sxs-lookup"><span data-stu-id="4c88d-145">C, F</span></span>  <br/> |
|<span data-ttu-id="4c88d-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="4c88d-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="4c88d-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="4c88d-147">xs:string</span></span>  <br/> |<span data-ttu-id="4c88d-148">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4c88d-148">required</span></span>  <br/> |<span data-ttu-id="4c88d-149">Spécifie l’URL de l’image pour l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="4c88d-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="4c88d-150">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="4c88d-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4c88d-151">fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="4c88d-151">timezone</span></span>  <br/> |<span data-ttu-id="4c88d-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4c88d-152">xs:integer</span></span>  <br/> |<span data-ttu-id="4c88d-153">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4c88d-153">required</span></span>  <br/> |<span data-ttu-id="4c88d-154">Spécifie le décalage GMT.</span><span class="sxs-lookup"><span data-stu-id="4c88d-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="4c88d-155">Une valeur comprise entre -11 et 12 inclus</span><span class="sxs-lookup"><span data-stu-id="4c88d-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="4c88d-156">url</span><span class="sxs-lookup"><span data-stu-id="4c88d-156">url</span></span>  <br/> |<span data-ttu-id="4c88d-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="4c88d-157">xs:string</span></span>  <br/> |<span data-ttu-id="4c88d-158">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4c88d-158">required</span></span>  <br/> |<span data-ttu-id="4c88d-159">Spécifie l’URL de la page web du service météo qui contient des informations météorologiques pour l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="4c88d-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="4c88d-160">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="4c88d-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4c88d-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="4c88d-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="4c88d-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="4c88d-162">xs:string</span></span>  <br/> |<span data-ttu-id="4c88d-163">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4c88d-163">required</span></span>  <br/> |<span data-ttu-id="4c88d-164">Spécifie le code qui est associé à l’emplacement permet de distinguer plusieurs emplacement ayant le même nom.</span><span class="sxs-lookup"><span data-stu-id="4c88d-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="4c88d-165">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="4c88d-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4c88d-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="4c88d-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="4c88d-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="4c88d-167">xs:string</span></span>  <br/> |<span data-ttu-id="4c88d-168">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4c88d-168">required</span></span>  <br/> |<span data-ttu-id="4c88d-169">Spécifie le nom de l’emplacement qui s’affiche dans le contrôle de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="4c88d-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="4c88d-170">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="4c88d-170">A value of the type xs:string</span></span>  <br/> |
   

