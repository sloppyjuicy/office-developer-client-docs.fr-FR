---
title: forecast element (weatherType complexType) (Outlook Weather Information Schema)
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
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="73338-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span><span class="sxs-lookup"><span data-stu-id="73338-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="73338-104">Spécifie les conditions météorologiques futures d’au moins trois jours à l’avance, y compris aujourd’hui : Aujourd’hui, Demain, Jour après Demain.</span><span class="sxs-lookup"><span data-stu-id="73338-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73338-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="73338-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73338-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="73338-106">**Element type**</span></span> <br/> |[<span data-ttu-id="73338-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="73338-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="73338-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="73338-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="73338-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="73338-109">**Schema file**</span></span> <br/> |<span data-ttu-id="73338-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="73338-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="73338-111">Définition</span><span class="sxs-lookup"><span data-stu-id="73338-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="73338-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="73338-112">Elements and attributes</span></span>

<span data-ttu-id="73338-113">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="73338-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="73338-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="73338-114">Parent elements</span></span>

|<span data-ttu-id="73338-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="73338-115">**Element**</span></span>|<span data-ttu-id="73338-116">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="73338-116">**Type**</span></span>|<span data-ttu-id="73338-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="73338-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="73338-118">météo</span><span class="sxs-lookup"><span data-stu-id="73338-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="73338-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="73338-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="73338-120">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="73338-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="73338-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="73338-121">Child elements</span></span>

<span data-ttu-id="73338-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="73338-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73338-123">Attributs</span><span class="sxs-lookup"><span data-stu-id="73338-123">Attributes</span></span>

|<span data-ttu-id="73338-124">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="73338-124">**Attribute**</span></span>|<span data-ttu-id="73338-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="73338-125">**Type**</span></span>|<span data-ttu-id="73338-126">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="73338-126">**Required**</span></span>|<span data-ttu-id="73338-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="73338-127">**Description**</span></span>|<span data-ttu-id="73338-128">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="73338-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="73338-129">date</span><span class="sxs-lookup"><span data-stu-id="73338-129">date</span></span>  <br/> |<span data-ttu-id="73338-130">xs:date</span><span class="sxs-lookup"><span data-stu-id="73338-130">xs:date</span></span>  <br/> |<span data-ttu-id="73338-131">obligatoire</span><span class="sxs-lookup"><span data-stu-id="73338-131">required</span></span>  <br/> |<span data-ttu-id="73338-132">Spécifie la date de la prévision.</span><span class="sxs-lookup"><span data-stu-id="73338-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="73338-133">Valeur du type xs:date</span><span class="sxs-lookup"><span data-stu-id="73338-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="73338-134">day</span><span class="sxs-lookup"><span data-stu-id="73338-134">day</span></span>  <br/> |<span data-ttu-id="73338-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="73338-135">xs:string</span></span>  <br/> |<span data-ttu-id="73338-136">obligatoire</span><span class="sxs-lookup"><span data-stu-id="73338-136">required</span></span>  <br/> |<span data-ttu-id="73338-137">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="73338-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="73338-138">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="73338-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="73338-139">high</span><span class="sxs-lookup"><span data-stu-id="73338-139">high</span></span>  <br/> |<span data-ttu-id="73338-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="73338-140">xs:integer</span></span>  <br/> |<span data-ttu-id="73338-141">obligatoire</span><span class="sxs-lookup"><span data-stu-id="73338-141">required</span></span>  <br/> |<span data-ttu-id="73338-142">Spécifie la température la plus élevée prévue.</span><span class="sxs-lookup"><span data-stu-id="73338-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="73338-143">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="73338-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="73338-144">faible</span><span class="sxs-lookup"><span data-stu-id="73338-144">low</span></span>  <br/> |<span data-ttu-id="73338-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="73338-145">xs:integer</span></span>  <br/> |<span data-ttu-id="73338-146">obligatoire</span><span class="sxs-lookup"><span data-stu-id="73338-146">required</span></span>  <br/> |<span data-ttu-id="73338-147">Spécifie la température la plus basse prévue.</span><span class="sxs-lookup"><span data-stu-id="73338-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="73338-148">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="73338-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="73338-149">precip</span><span class="sxs-lookup"><span data-stu-id="73338-149">precip</span></span>  <br/> |<span data-ttu-id="73338-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="73338-150">xs:integer</span></span>  <br/> |<span data-ttu-id="73338-151">obligatoire</span><span class="sxs-lookup"><span data-stu-id="73338-151">required</span></span>  <br/> |<span data-ttu-id="73338-152">Spécifie la possibilité de pourcentage d’éventualité.</span><span class="sxs-lookup"><span data-stu-id="73338-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="73338-153">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="73338-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="73338-154">shortday</span><span class="sxs-lookup"><span data-stu-id="73338-154">shortday</span></span>  <br/> |<span data-ttu-id="73338-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="73338-155">xs:string</span></span>  <br/> |<span data-ttu-id="73338-156">obligatoire</span><span class="sxs-lookup"><span data-stu-id="73338-156">required</span></span>  <br/> |<span data-ttu-id="73338-157">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="73338-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="73338-158">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="73338-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="73338-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="73338-159">skycodeday</span></span>  <br/> |<span data-ttu-id="73338-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="73338-160">xs:integer</span></span>  <br/> |<span data-ttu-id="73338-161">obligatoire</span><span class="sxs-lookup"><span data-stu-id="73338-161">required</span></span>  <br/> |<span data-ttu-id="73338-162">Spécifie un code pour les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="73338-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="73338-163">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="73338-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="73338-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="73338-164">skytextday</span></span>  <br/> |<span data-ttu-id="73338-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="73338-165">xs:string</span></span>  <br/> |<span data-ttu-id="73338-166">obligatoire</span><span class="sxs-lookup"><span data-stu-id="73338-166">required</span></span>  <br/> |<span data-ttu-id="73338-167">Spécifie un à deux mots qui décrivent les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="73338-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="73338-168">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="73338-168">A value of the type xs:string</span></span>  <br/> |
   

