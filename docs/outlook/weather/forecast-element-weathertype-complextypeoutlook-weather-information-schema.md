---
title: Forecast, élément (weatherType complexType) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: "Spécifie les conditions météorologiques futures d'une avance de trois jours, y compris aujourd'hui: aujourd'hui, demain, jour après demain."
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339563"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="782bd-103">Forecast, élément (weatherType complexType) (Outlook Weather Information Schema)</span><span class="sxs-lookup"><span data-stu-id="782bd-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="782bd-104">Spécifie les conditions météorologiques futures d'une avance de trois jours, y compris aujourd'hui: aujourd'hui, demain, jour après demain.</span><span class="sxs-lookup"><span data-stu-id="782bd-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="782bd-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="782bd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="782bd-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="782bd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="782bd-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="782bd-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="782bd-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="782bd-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="782bd-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="782bd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="782bd-110">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="782bd-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="782bd-111">Définition</span><span class="sxs-lookup"><span data-stu-id="782bd-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="782bd-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="782bd-112">Elements and attributes</span></span>

<span data-ttu-id="782bd-113">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="782bd-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="782bd-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="782bd-114">Parent elements</span></span>

|<span data-ttu-id="782bd-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="782bd-115">**Element**</span></span>|<span data-ttu-id="782bd-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="782bd-116">**Type**</span></span>|<span data-ttu-id="782bd-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="782bd-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="782bd-118">renseignement</span><span class="sxs-lookup"><span data-stu-id="782bd-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="782bd-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="782bd-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="782bd-120">Spécifie les conditions météorologiques d'un emplacement.</span><span class="sxs-lookup"><span data-stu-id="782bd-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="782bd-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="782bd-121">Child elements</span></span>

<span data-ttu-id="782bd-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="782bd-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="782bd-123">Attributs</span><span class="sxs-lookup"><span data-stu-id="782bd-123">Attributes</span></span>

|<span data-ttu-id="782bd-124">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="782bd-124">**Attribute**</span></span>|<span data-ttu-id="782bd-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="782bd-125">**Type**</span></span>|<span data-ttu-id="782bd-126">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="782bd-126">**Required**</span></span>|<span data-ttu-id="782bd-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="782bd-127">**Description**</span></span>|<span data-ttu-id="782bd-128">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="782bd-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="782bd-129">date</span><span class="sxs-lookup"><span data-stu-id="782bd-129">date</span></span>  <br/> |<span data-ttu-id="782bd-130">XS: date</span><span class="sxs-lookup"><span data-stu-id="782bd-130">xs:date</span></span>  <br/> |<span data-ttu-id="782bd-131">obligatoire</span><span class="sxs-lookup"><span data-stu-id="782bd-131">required</span></span>  <br/> |<span data-ttu-id="782bd-132">Indique la date de la prévision.</span><span class="sxs-lookup"><span data-stu-id="782bd-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="782bd-133">Une valeur de type xs: date</span><span class="sxs-lookup"><span data-stu-id="782bd-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="782bd-134">quotidienne</span><span class="sxs-lookup"><span data-stu-id="782bd-134">day</span></span>  <br/> |<span data-ttu-id="782bd-135">XS: String</span><span class="sxs-lookup"><span data-stu-id="782bd-135">xs:string</span></span>  <br/> |<span data-ttu-id="782bd-136">obligatoire</span><span class="sxs-lookup"><span data-stu-id="782bd-136">required</span></span>  <br/> |<span data-ttu-id="782bd-137">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="782bd-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="782bd-138">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="782bd-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="782bd-139">important</span><span class="sxs-lookup"><span data-stu-id="782bd-139">high</span></span>  <br/> |<span data-ttu-id="782bd-140">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="782bd-140">xs:integer</span></span>  <br/> |<span data-ttu-id="782bd-141">obligatoire</span><span class="sxs-lookup"><span data-stu-id="782bd-141">required</span></span>  <br/> |<span data-ttu-id="782bd-142">Spécifie la température la plus élevée prévue.</span><span class="sxs-lookup"><span data-stu-id="782bd-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="782bd-143">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="782bd-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="782bd-144">assez</span><span class="sxs-lookup"><span data-stu-id="782bd-144">low</span></span>  <br/> |<span data-ttu-id="782bd-145">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="782bd-145">xs:integer</span></span>  <br/> |<span data-ttu-id="782bd-146">obligatoire</span><span class="sxs-lookup"><span data-stu-id="782bd-146">required</span></span>  <br/> |<span data-ttu-id="782bd-147">Spécifie la température minimale prévue.</span><span class="sxs-lookup"><span data-stu-id="782bd-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="782bd-148">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="782bd-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="782bd-149">PRECIP</span><span class="sxs-lookup"><span data-stu-id="782bd-149">precip</span></span>  <br/> |<span data-ttu-id="782bd-150">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="782bd-150">xs:integer</span></span>  <br/> |<span data-ttu-id="782bd-151">obligatoire</span><span class="sxs-lookup"><span data-stu-id="782bd-151">required</span></span>  <br/> |<span data-ttu-id="782bd-152">Indique le pourcentage de probabilité de précipitation.</span><span class="sxs-lookup"><span data-stu-id="782bd-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="782bd-153">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="782bd-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="782bd-154">shortday</span><span class="sxs-lookup"><span data-stu-id="782bd-154">shortday</span></span>  <br/> |<span data-ttu-id="782bd-155">XS: String</span><span class="sxs-lookup"><span data-stu-id="782bd-155">xs:string</span></span>  <br/> |<span data-ttu-id="782bd-156">obligatoire</span><span class="sxs-lookup"><span data-stu-id="782bd-156">required</span></span>  <br/> |<span data-ttu-id="782bd-157">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="782bd-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="782bd-158">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="782bd-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="782bd-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="782bd-159">skycodeday</span></span>  <br/> |<span data-ttu-id="782bd-160">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="782bd-160">xs:integer</span></span>  <br/> |<span data-ttu-id="782bd-161">obligatoire</span><span class="sxs-lookup"><span data-stu-id="782bd-161">required</span></span>  <br/> |<span data-ttu-id="782bd-162">Spécifie un code pour les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="782bd-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="782bd-163">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="782bd-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="782bd-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="782bd-164">skytextday</span></span>  <br/> |<span data-ttu-id="782bd-165">XS: String</span><span class="sxs-lookup"><span data-stu-id="782bd-165">xs:string</span></span>  <br/> |<span data-ttu-id="782bd-166">obligatoire</span><span class="sxs-lookup"><span data-stu-id="782bd-166">required</span></span>  <br/> |<span data-ttu-id="782bd-167">Spécifie un à deux mots qui décrivent les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="782bd-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="782bd-168">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="782bd-168">A value of the type xs:string</span></span>  <br/> |
   

