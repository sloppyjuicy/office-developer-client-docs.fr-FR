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
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390624"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="dabcc-103">type complexe forecastType (schéma des informations météo Outlook)</span><span class="sxs-lookup"><span data-stu-id="dabcc-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="dabcc-104">Définit les paramètres sur les conditions de prévisions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="dabcc-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="dabcc-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="dabcc-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dabcc-106">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="dabcc-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="dabcc-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="dabcc-107">**Schema file**</span></span> <br/> |<span data-ttu-id="dabcc-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="dabcc-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="dabcc-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="dabcc-109">**Extension base**</span></span> <br/> |<span data-ttu-id="dabcc-110">Aucune</span><span class="sxs-lookup"><span data-stu-id="dabcc-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dabcc-111">Définition</span><span class="sxs-lookup"><span data-stu-id="dabcc-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="dabcc-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="dabcc-112">Elements and attributes</span></span>

<span data-ttu-id="dabcc-113">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="dabcc-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="dabcc-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dabcc-114">Child elements</span></span>

<span data-ttu-id="dabcc-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dabcc-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dabcc-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="dabcc-116">Attributes</span></span>

|<span data-ttu-id="dabcc-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dabcc-117">**Attribute**</span></span>|<span data-ttu-id="dabcc-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="dabcc-118">**Type**</span></span>|<span data-ttu-id="dabcc-119">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="dabcc-119">**Required**</span></span>|<span data-ttu-id="dabcc-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="dabcc-120">**Description**</span></span>|<span data-ttu-id="dabcc-121">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="dabcc-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dabcc-122">date</span><span class="sxs-lookup"><span data-stu-id="dabcc-122">date</span></span>  <br/> |<span data-ttu-id="dabcc-123">xs : date</span><span class="sxs-lookup"><span data-stu-id="dabcc-123">xs:date</span></span>  <br/> |<span data-ttu-id="dabcc-124">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dabcc-124">required</span></span>  <br/> |<span data-ttu-id="dabcc-125">Spécifie la date pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="dabcc-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="dabcc-126">Valeur du type xs : date</span><span class="sxs-lookup"><span data-stu-id="dabcc-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="dabcc-127">jour</span><span class="sxs-lookup"><span data-stu-id="dabcc-127">day</span></span>  <br/> |<span data-ttu-id="dabcc-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="dabcc-128">xs:string</span></span>  <br/> |<span data-ttu-id="dabcc-129">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dabcc-129">required</span></span>  <br/> |<span data-ttu-id="dabcc-130">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="dabcc-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="dabcc-131">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="dabcc-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="dabcc-132">haute</span><span class="sxs-lookup"><span data-stu-id="dabcc-132">high</span></span>  <br/> |<span data-ttu-id="dabcc-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dabcc-133">xs:integer</span></span>  <br/> |<span data-ttu-id="dabcc-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dabcc-134">required</span></span>  <br/> |<span data-ttu-id="dabcc-135">Spécifie la température la plus élevée prévue.</span><span class="sxs-lookup"><span data-stu-id="dabcc-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="dabcc-136">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="dabcc-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="dabcc-137">faible</span><span class="sxs-lookup"><span data-stu-id="dabcc-137">low</span></span>  <br/> |<span data-ttu-id="dabcc-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dabcc-138">xs:integer</span></span>  <br/> |<span data-ttu-id="dabcc-139">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dabcc-139">required</span></span>  <br/> |<span data-ttu-id="dabcc-140">Spécifie la température prévue.</span><span class="sxs-lookup"><span data-stu-id="dabcc-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="dabcc-141">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="dabcc-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="dabcc-142">precip</span><span class="sxs-lookup"><span data-stu-id="dabcc-142">precip</span></span>  <br/> |<span data-ttu-id="dabcc-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dabcc-143">xs:integer</span></span>  <br/> |<span data-ttu-id="dabcc-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dabcc-144">required</span></span>  <br/> |<span data-ttu-id="dabcc-145">Spécifie la possibilité de pourcentage de précipitation.</span><span class="sxs-lookup"><span data-stu-id="dabcc-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="dabcc-146">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="dabcc-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="dabcc-147">shortday</span><span class="sxs-lookup"><span data-stu-id="dabcc-147">shortday</span></span>  <br/> |<span data-ttu-id="dabcc-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="dabcc-148">xs:string</span></span>  <br/> |<span data-ttu-id="dabcc-149">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dabcc-149">required</span></span>  <br/> |<span data-ttu-id="dabcc-150">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="dabcc-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="dabcc-151">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="dabcc-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="dabcc-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="dabcc-152">skycodeday</span></span>  <br/> |<span data-ttu-id="dabcc-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dabcc-153">xs:integer</span></span>  <br/> |<span data-ttu-id="dabcc-154">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dabcc-154">required</span></span>  <br/> |<span data-ttu-id="dabcc-155">Spécifie un code pour les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="dabcc-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="dabcc-156">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="dabcc-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="dabcc-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="dabcc-157">skytextday</span></span>  <br/> |<span data-ttu-id="dabcc-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="dabcc-158">xs:string</span></span>  <br/> |<span data-ttu-id="dabcc-159">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dabcc-159">required</span></span>  <br/> |<span data-ttu-id="dabcc-160">Spécifie un ou deux mots qui décrivent les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="dabcc-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="dabcc-161">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="dabcc-161">A value of the type xs:string</span></span>  <br/> |
   

