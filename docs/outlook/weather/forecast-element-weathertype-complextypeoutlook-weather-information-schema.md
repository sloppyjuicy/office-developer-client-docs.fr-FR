---
title: Forecast, élément (weatherType complexType) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Spécifie les conditions météorologiques futures d’une avance de trois jours, y compris aujourd’hui: aujourd’hui, demain, jour après demain.'
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540979"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="40343-103">Forecast, élément (weatherType complexType) (Outlook Weather Information Schema)</span><span class="sxs-lookup"><span data-stu-id="40343-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="40343-104">Spécifie les conditions météorologiques futures d’une avance de trois jours, y compris aujourd’hui: aujourd’hui, demain, jour après demain.</span><span class="sxs-lookup"><span data-stu-id="40343-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40343-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="40343-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40343-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="40343-106">**Element type**</span></span> <br/> |[<span data-ttu-id="40343-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="40343-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="40343-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="40343-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="40343-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="40343-109">**Schema file**</span></span> <br/> |<span data-ttu-id="40343-110">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="40343-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="40343-111">Définition</span><span class="sxs-lookup"><span data-stu-id="40343-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="40343-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="40343-112">Elements and attributes</span></span>

<span data-ttu-id="40343-113">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="40343-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="40343-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="40343-114">Parent elements</span></span>

|<span data-ttu-id="40343-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="40343-115">**Element**</span></span>|<span data-ttu-id="40343-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="40343-116">**Type**</span></span>|<span data-ttu-id="40343-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="40343-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="40343-118">renseignement</span><span class="sxs-lookup"><span data-stu-id="40343-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="40343-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="40343-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="40343-120">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="40343-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="40343-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="40343-121">Child elements</span></span>

<span data-ttu-id="40343-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="40343-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40343-123">Attributs</span><span class="sxs-lookup"><span data-stu-id="40343-123">Attributes</span></span>

|<span data-ttu-id="40343-124">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="40343-124">**Attribute**</span></span>|<span data-ttu-id="40343-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="40343-125">**Type**</span></span>|<span data-ttu-id="40343-126">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="40343-126">**Required**</span></span>|<span data-ttu-id="40343-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="40343-127">**Description**</span></span>|<span data-ttu-id="40343-128">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="40343-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="40343-129">date</span><span class="sxs-lookup"><span data-stu-id="40343-129">date</span></span>  <br/> |<span data-ttu-id="40343-130">XS: date</span><span class="sxs-lookup"><span data-stu-id="40343-130">xs:date</span></span>  <br/> |<span data-ttu-id="40343-131">obligatoire</span><span class="sxs-lookup"><span data-stu-id="40343-131">required</span></span>  <br/> |<span data-ttu-id="40343-132">Indique la date de la prévision.</span><span class="sxs-lookup"><span data-stu-id="40343-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="40343-133">Une valeur de type xs: date</span><span class="sxs-lookup"><span data-stu-id="40343-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="40343-134">quotidienne</span><span class="sxs-lookup"><span data-stu-id="40343-134">day</span></span>  <br/> |<span data-ttu-id="40343-135">XS: String</span><span class="sxs-lookup"><span data-stu-id="40343-135">xs:string</span></span>  <br/> |<span data-ttu-id="40343-136">obligatoire</span><span class="sxs-lookup"><span data-stu-id="40343-136">required</span></span>  <br/> |<span data-ttu-id="40343-137">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="40343-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="40343-138">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="40343-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="40343-139">important</span><span class="sxs-lookup"><span data-stu-id="40343-139">high</span></span>  <br/> |<span data-ttu-id="40343-140">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="40343-140">xs:integer</span></span>  <br/> |<span data-ttu-id="40343-141">obligatoire</span><span class="sxs-lookup"><span data-stu-id="40343-141">required</span></span>  <br/> |<span data-ttu-id="40343-142">Spécifie la température la plus élevée prévue.</span><span class="sxs-lookup"><span data-stu-id="40343-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="40343-143">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="40343-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="40343-144">assez</span><span class="sxs-lookup"><span data-stu-id="40343-144">low</span></span>  <br/> |<span data-ttu-id="40343-145">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="40343-145">xs:integer</span></span>  <br/> |<span data-ttu-id="40343-146">obligatoire</span><span class="sxs-lookup"><span data-stu-id="40343-146">required</span></span>  <br/> |<span data-ttu-id="40343-147">Spécifie la température minimale prévue.</span><span class="sxs-lookup"><span data-stu-id="40343-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="40343-148">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="40343-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="40343-149">precip</span><span class="sxs-lookup"><span data-stu-id="40343-149">precip</span></span>  <br/> |<span data-ttu-id="40343-150">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="40343-150">xs:integer</span></span>  <br/> |<span data-ttu-id="40343-151">obligatoire</span><span class="sxs-lookup"><span data-stu-id="40343-151">required</span></span>  <br/> |<span data-ttu-id="40343-152">Indique le pourcentage de probabilité de précipitation.</span><span class="sxs-lookup"><span data-stu-id="40343-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="40343-153">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="40343-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="40343-154">shortday</span><span class="sxs-lookup"><span data-stu-id="40343-154">shortday</span></span>  <br/> |<span data-ttu-id="40343-155">XS: String</span><span class="sxs-lookup"><span data-stu-id="40343-155">xs:string</span></span>  <br/> |<span data-ttu-id="40343-156">obligatoire</span><span class="sxs-lookup"><span data-stu-id="40343-156">required</span></span>  <br/> |<span data-ttu-id="40343-157">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="40343-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="40343-158">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="40343-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="40343-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="40343-159">skycodeday</span></span>  <br/> |<span data-ttu-id="40343-160">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="40343-160">xs:integer</span></span>  <br/> |<span data-ttu-id="40343-161">obligatoire</span><span class="sxs-lookup"><span data-stu-id="40343-161">required</span></span>  <br/> |<span data-ttu-id="40343-162">Spécifie un code pour les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="40343-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="40343-163">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="40343-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="40343-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="40343-164">skytextday</span></span>  <br/> |<span data-ttu-id="40343-165">XS: String</span><span class="sxs-lookup"><span data-stu-id="40343-165">xs:string</span></span>  <br/> |<span data-ttu-id="40343-166">obligatoire</span><span class="sxs-lookup"><span data-stu-id="40343-166">required</span></span>  <br/> |<span data-ttu-id="40343-167">Spécifie un à deux mots qui décrivent les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="40343-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="40343-168">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="40343-168">A value of the type xs:string</span></span>  <br/> |
   

