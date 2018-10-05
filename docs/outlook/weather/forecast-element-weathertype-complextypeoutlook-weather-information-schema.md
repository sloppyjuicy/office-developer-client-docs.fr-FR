---
title: prévision, élément (weatherType, complexType) (schéma des informations météo Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: "Spécifie les conditions météo future d’au moins trois jours avance y compris aujourd'hui : aujourd'hui, demain, jour après demain."
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398324"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="2c711-103">prévision, élément (weatherType, complexType) (schéma des informations météo Outlook)</span><span class="sxs-lookup"><span data-stu-id="2c711-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="2c711-104">Spécifie les conditions météo future d’au moins trois jours avance y compris aujourd'hui : aujourd'hui, demain, jour après demain.</span><span class="sxs-lookup"><span data-stu-id="2c711-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c711-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="2c711-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c711-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="2c711-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2c711-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="2c711-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="2c711-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="2c711-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="2c711-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="2c711-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2c711-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="2c711-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2c711-111">Définition</span><span class="sxs-lookup"><span data-stu-id="2c711-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="2c711-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="2c711-112">Elements and attributes</span></span>

<span data-ttu-id="2c711-113">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="2c711-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2c711-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2c711-114">Parent elements</span></span>

|<span data-ttu-id="2c711-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2c711-115">**Element**</span></span>|<span data-ttu-id="2c711-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="2c711-116">**Type**</span></span>|<span data-ttu-id="2c711-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="2c711-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2c711-118">météo</span><span class="sxs-lookup"><span data-stu-id="2c711-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="2c711-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="2c711-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="2c711-120">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="2c711-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2c711-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2c711-121">Child elements</span></span>

<span data-ttu-id="2c711-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2c711-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c711-123">Attributs</span><span class="sxs-lookup"><span data-stu-id="2c711-123">Attributes</span></span>

|<span data-ttu-id="2c711-124">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2c711-124">**Attribute**</span></span>|<span data-ttu-id="2c711-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="2c711-125">**Type**</span></span>|<span data-ttu-id="2c711-126">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="2c711-126">**Required**</span></span>|<span data-ttu-id="2c711-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="2c711-127">**Description**</span></span>|<span data-ttu-id="2c711-128">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2c711-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2c711-129">date</span><span class="sxs-lookup"><span data-stu-id="2c711-129">date</span></span>  <br/> |<span data-ttu-id="2c711-130">xs : date</span><span class="sxs-lookup"><span data-stu-id="2c711-130">xs:date</span></span>  <br/> |<span data-ttu-id="2c711-131">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2c711-131">required</span></span>  <br/> |<span data-ttu-id="2c711-132">Spécifie la date pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="2c711-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="2c711-133">Valeur du type xs : date</span><span class="sxs-lookup"><span data-stu-id="2c711-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="2c711-134">jour</span><span class="sxs-lookup"><span data-stu-id="2c711-134">day</span></span>  <br/> |<span data-ttu-id="2c711-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="2c711-135">xs:string</span></span>  <br/> |<span data-ttu-id="2c711-136">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2c711-136">required</span></span>  <br/> |<span data-ttu-id="2c711-137">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="2c711-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="2c711-138">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="2c711-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="2c711-139">haute</span><span class="sxs-lookup"><span data-stu-id="2c711-139">high</span></span>  <br/> |<span data-ttu-id="2c711-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2c711-140">xs:integer</span></span>  <br/> |<span data-ttu-id="2c711-141">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2c711-141">required</span></span>  <br/> |<span data-ttu-id="2c711-142">Spécifie la température la plus élevée prévue.</span><span class="sxs-lookup"><span data-stu-id="2c711-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="2c711-143">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="2c711-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2c711-144">faible</span><span class="sxs-lookup"><span data-stu-id="2c711-144">low</span></span>  <br/> |<span data-ttu-id="2c711-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2c711-145">xs:integer</span></span>  <br/> |<span data-ttu-id="2c711-146">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2c711-146">required</span></span>  <br/> |<span data-ttu-id="2c711-147">Spécifie la température prévue.</span><span class="sxs-lookup"><span data-stu-id="2c711-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="2c711-148">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="2c711-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2c711-149">precip</span><span class="sxs-lookup"><span data-stu-id="2c711-149">precip</span></span>  <br/> |<span data-ttu-id="2c711-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2c711-150">xs:integer</span></span>  <br/> |<span data-ttu-id="2c711-151">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2c711-151">required</span></span>  <br/> |<span data-ttu-id="2c711-152">Spécifie la possibilité de pourcentage de précipitation.</span><span class="sxs-lookup"><span data-stu-id="2c711-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="2c711-153">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="2c711-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2c711-154">shortday</span><span class="sxs-lookup"><span data-stu-id="2c711-154">shortday</span></span>  <br/> |<span data-ttu-id="2c711-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="2c711-155">xs:string</span></span>  <br/> |<span data-ttu-id="2c711-156">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2c711-156">required</span></span>  <br/> |<span data-ttu-id="2c711-157">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="2c711-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="2c711-158">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="2c711-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="2c711-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="2c711-159">skycodeday</span></span>  <br/> |<span data-ttu-id="2c711-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2c711-160">xs:integer</span></span>  <br/> |<span data-ttu-id="2c711-161">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2c711-161">required</span></span>  <br/> |<span data-ttu-id="2c711-162">Spécifie un code pour les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="2c711-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="2c711-163">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="2c711-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2c711-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="2c711-164">skytextday</span></span>  <br/> |<span data-ttu-id="2c711-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="2c711-165">xs:string</span></span>  <br/> |<span data-ttu-id="2c711-166">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2c711-166">required</span></span>  <br/> |<span data-ttu-id="2c711-167">Spécifie un ou deux mots qui décrivent les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="2c711-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="2c711-168">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="2c711-168">A value of the type xs:string</span></span>  <br/> |
   

