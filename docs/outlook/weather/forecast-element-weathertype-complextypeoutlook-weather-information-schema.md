---
title: forecast, élément (weatherType complexType) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Spécifie les conditions météorologiques futures d’au moins trois jours à l’avance, y compris aujourd’hui : Aujourd’hui, Demain, Jour après Demain.'
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540979"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="d938f-103">forecast, élément (weatherType complexType) (Outlook Weather Information Schema)</span><span class="sxs-lookup"><span data-stu-id="d938f-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="d938f-104">Spécifie les conditions météorologiques futures d’au moins trois jours à l’avance, y compris aujourd’hui : Aujourd’hui, Demain, Jour après Demain.</span><span class="sxs-lookup"><span data-stu-id="d938f-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d938f-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="d938f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d938f-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="d938f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d938f-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="d938f-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="d938f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d938f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="d938f-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d938f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d938f-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="d938f-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d938f-111">Définition</span><span class="sxs-lookup"><span data-stu-id="d938f-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="d938f-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d938f-112">Elements and attributes</span></span>

<span data-ttu-id="d938f-113">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="d938f-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d938f-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d938f-114">Parent elements</span></span>

|<span data-ttu-id="d938f-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d938f-115">**Element**</span></span>|<span data-ttu-id="d938f-116">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="d938f-116">**Type**</span></span>|<span data-ttu-id="d938f-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="d938f-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d938f-118">météo</span><span class="sxs-lookup"><span data-stu-id="d938f-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="d938f-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="d938f-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="d938f-120">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="d938f-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d938f-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d938f-121">Child elements</span></span>

<span data-ttu-id="d938f-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d938f-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d938f-123">Attributs</span><span class="sxs-lookup"><span data-stu-id="d938f-123">Attributes</span></span>

|<span data-ttu-id="d938f-124">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d938f-124">**Attribute**</span></span>|<span data-ttu-id="d938f-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="d938f-125">**Type**</span></span>|<span data-ttu-id="d938f-126">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d938f-126">**Required**</span></span>|<span data-ttu-id="d938f-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="d938f-127">**Description**</span></span>|<span data-ttu-id="d938f-128">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="d938f-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d938f-129">date</span><span class="sxs-lookup"><span data-stu-id="d938f-129">date</span></span>  <br/> |<span data-ttu-id="d938f-130">xs:date</span><span class="sxs-lookup"><span data-stu-id="d938f-130">xs:date</span></span>  <br/> |<span data-ttu-id="d938f-131">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d938f-131">required</span></span>  <br/> |<span data-ttu-id="d938f-132">Spécifie la date de la prévision.</span><span class="sxs-lookup"><span data-stu-id="d938f-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="d938f-133">Valeur du type xs:date</span><span class="sxs-lookup"><span data-stu-id="d938f-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="d938f-134">day</span><span class="sxs-lookup"><span data-stu-id="d938f-134">day</span></span>  <br/> |<span data-ttu-id="d938f-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="d938f-135">xs:string</span></span>  <br/> |<span data-ttu-id="d938f-136">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d938f-136">required</span></span>  <br/> |<span data-ttu-id="d938f-137">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="d938f-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="d938f-138">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="d938f-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d938f-139">high</span><span class="sxs-lookup"><span data-stu-id="d938f-139">high</span></span>  <br/> |<span data-ttu-id="d938f-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d938f-140">xs:integer</span></span>  <br/> |<span data-ttu-id="d938f-141">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d938f-141">required</span></span>  <br/> |<span data-ttu-id="d938f-142">Spécifie la température la plus élevée prévue.</span><span class="sxs-lookup"><span data-stu-id="d938f-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="d938f-143">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="d938f-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d938f-144">faible</span><span class="sxs-lookup"><span data-stu-id="d938f-144">low</span></span>  <br/> |<span data-ttu-id="d938f-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d938f-145">xs:integer</span></span>  <br/> |<span data-ttu-id="d938f-146">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d938f-146">required</span></span>  <br/> |<span data-ttu-id="d938f-147">Spécifie la température la plus basse prévue.</span><span class="sxs-lookup"><span data-stu-id="d938f-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="d938f-148">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="d938f-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d938f-149">precip</span><span class="sxs-lookup"><span data-stu-id="d938f-149">precip</span></span>  <br/> |<span data-ttu-id="d938f-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d938f-150">xs:integer</span></span>  <br/> |<span data-ttu-id="d938f-151">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d938f-151">required</span></span>  <br/> |<span data-ttu-id="d938f-152">Spécifie la possibilité de pourcentage d’éventualité.</span><span class="sxs-lookup"><span data-stu-id="d938f-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="d938f-153">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="d938f-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d938f-154">shortday</span><span class="sxs-lookup"><span data-stu-id="d938f-154">shortday</span></span>  <br/> |<span data-ttu-id="d938f-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="d938f-155">xs:string</span></span>  <br/> |<span data-ttu-id="d938f-156">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d938f-156">required</span></span>  <br/> |<span data-ttu-id="d938f-157">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="d938f-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="d938f-158">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="d938f-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d938f-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="d938f-159">skycodeday</span></span>  <br/> |<span data-ttu-id="d938f-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d938f-160">xs:integer</span></span>  <br/> |<span data-ttu-id="d938f-161">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d938f-161">required</span></span>  <br/> |<span data-ttu-id="d938f-162">Spécifie un code pour les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="d938f-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="d938f-163">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="d938f-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d938f-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="d938f-164">skytextday</span></span>  <br/> |<span data-ttu-id="d938f-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="d938f-165">xs:string</span></span>  <br/> |<span data-ttu-id="d938f-166">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d938f-166">required</span></span>  <br/> |<span data-ttu-id="d938f-167">Spécifie un à deux mots qui décrivent les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="d938f-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="d938f-168">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="d938f-168">A value of the type xs:string</span></span>  <br/> |
   

