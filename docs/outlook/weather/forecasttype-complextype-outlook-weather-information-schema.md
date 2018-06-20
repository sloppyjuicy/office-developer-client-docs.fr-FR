---
title: type complexe forecastType (schéma des informations météo Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Définit les paramètres sur les conditions de prévisions météorologiques d’un emplacement.
ms.openlocfilehash: 886c6cdbbeb9f07564854dc6a62cbcdad9703b62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787714"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="41c2a-103">type complexe forecastType (schéma des informations météo Outlook)</span><span class="sxs-lookup"><span data-stu-id="41c2a-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="41c2a-104">Définit les paramètres sur les conditions de prévisions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="41c2a-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="41c2a-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="41c2a-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41c2a-106">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="41c2a-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="41c2a-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="41c2a-107">**Schema file**</span></span> <br/> |<span data-ttu-id="41c2a-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="41c2a-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="41c2a-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="41c2a-109">**Extension base**</span></span> <br/> |<span data-ttu-id="41c2a-110">Aucune</span><span class="sxs-lookup"><span data-stu-id="41c2a-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="41c2a-111">Définition</span><span class="sxs-lookup"><span data-stu-id="41c2a-111">Definition</span></span>

```XML
       <xs:complexType name="forecastType">
     <xs:attribute name="shortday"   type="xs:string"      use="required"     />
     <xs:attribute name="day"   type="xs:string"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="precip"   type="xs:integer"      use="required"     />
     <xs:attribute name="skytextday"   type="xs:string"      use="required"     />
     <xs:attribute name="skycodeday"   type="xs:integer"      use="required"     />
     <xs:attribute name="high"   type="xs:integer"      use="required"     />
     <xs:attribute name="low"   type="xs:integer"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="41c2a-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="41c2a-112">Elements and attributes</span></span>

<span data-ttu-id="41c2a-113">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="41c2a-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="41c2a-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="41c2a-114">Child elements</span></span>

<span data-ttu-id="41c2a-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="41c2a-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41c2a-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="41c2a-116">Attributes</span></span>

|<span data-ttu-id="41c2a-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="41c2a-117">**Attribute**</span></span>|<span data-ttu-id="41c2a-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="41c2a-118">**Type**</span></span>|<span data-ttu-id="41c2a-119">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="41c2a-119">**Required**</span></span>|<span data-ttu-id="41c2a-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="41c2a-120">**Description**</span></span>|<span data-ttu-id="41c2a-121">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="41c2a-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="41c2a-122">date</span><span class="sxs-lookup"><span data-stu-id="41c2a-122">date</span></span>  <br/> |<span data-ttu-id="41c2a-123">xs : date</span><span class="sxs-lookup"><span data-stu-id="41c2a-123">xs:date</span></span>  <br/> |<span data-ttu-id="41c2a-124">obligatoire</span><span class="sxs-lookup"><span data-stu-id="41c2a-124">required</span></span>  <br/> |<span data-ttu-id="41c2a-125">Spécifie la date pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="41c2a-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="41c2a-126">Valeur du type xs : date</span><span class="sxs-lookup"><span data-stu-id="41c2a-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="41c2a-127">jour</span><span class="sxs-lookup"><span data-stu-id="41c2a-127">day</span></span>  <br/> |<span data-ttu-id="41c2a-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="41c2a-128">xs:string</span></span>  <br/> |<span data-ttu-id="41c2a-129">obligatoire</span><span class="sxs-lookup"><span data-stu-id="41c2a-129">required</span></span>  <br/> |<span data-ttu-id="41c2a-130">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="41c2a-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="41c2a-131">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="41c2a-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="41c2a-132">haute</span><span class="sxs-lookup"><span data-stu-id="41c2a-132">high</span></span>  <br/> |<span data-ttu-id="41c2a-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="41c2a-133">xs:integer</span></span>  <br/> |<span data-ttu-id="41c2a-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="41c2a-134">required</span></span>  <br/> |<span data-ttu-id="41c2a-135">Spécifie la température la plus élevée prévue.</span><span class="sxs-lookup"><span data-stu-id="41c2a-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="41c2a-136">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="41c2a-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="41c2a-137">faible</span><span class="sxs-lookup"><span data-stu-id="41c2a-137">low</span></span>  <br/> |<span data-ttu-id="41c2a-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="41c2a-138">xs:integer</span></span>  <br/> |<span data-ttu-id="41c2a-139">obligatoire</span><span class="sxs-lookup"><span data-stu-id="41c2a-139">required</span></span>  <br/> |<span data-ttu-id="41c2a-140">Spécifie la température prévue.</span><span class="sxs-lookup"><span data-stu-id="41c2a-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="41c2a-141">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="41c2a-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="41c2a-142">precip</span><span class="sxs-lookup"><span data-stu-id="41c2a-142">precip</span></span>  <br/> |<span data-ttu-id="41c2a-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="41c2a-143">xs:integer</span></span>  <br/> |<span data-ttu-id="41c2a-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="41c2a-144">required</span></span>  <br/> |<span data-ttu-id="41c2a-145">Spécifie la possibilité de pourcentage de précipitation.</span><span class="sxs-lookup"><span data-stu-id="41c2a-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="41c2a-146">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="41c2a-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="41c2a-147">shortday</span><span class="sxs-lookup"><span data-stu-id="41c2a-147">shortday</span></span>  <br/> |<span data-ttu-id="41c2a-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="41c2a-148">xs:string</span></span>  <br/> |<span data-ttu-id="41c2a-149">obligatoire</span><span class="sxs-lookup"><span data-stu-id="41c2a-149">required</span></span>  <br/> |<span data-ttu-id="41c2a-150">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="41c2a-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="41c2a-151">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="41c2a-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="41c2a-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="41c2a-152">skycodeday</span></span>  <br/> |<span data-ttu-id="41c2a-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="41c2a-153">xs:integer</span></span>  <br/> |<span data-ttu-id="41c2a-154">obligatoire</span><span class="sxs-lookup"><span data-stu-id="41c2a-154">required</span></span>  <br/> |<span data-ttu-id="41c2a-155">Spécifie un code pour les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="41c2a-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="41c2a-156">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="41c2a-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="41c2a-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="41c2a-157">skytextday</span></span>  <br/> |<span data-ttu-id="41c2a-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="41c2a-158">xs:string</span></span>  <br/> |<span data-ttu-id="41c2a-159">obligatoire</span><span class="sxs-lookup"><span data-stu-id="41c2a-159">required</span></span>  <br/> |<span data-ttu-id="41c2a-160">Spécifie un ou deux mots qui décrivent les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="41c2a-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="41c2a-161">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="41c2a-161">A value of the type xs:string</span></span>  <br/> |
   

