---
title: complexType forecastType (schéma d'informations météorologiques Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Définit les paramètres relatifs aux conditions météorologiques de prévision d'un emplacement.
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361144"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="22960-103">complexType forecastType (schéma d'informations météorologiques Outlook)</span><span class="sxs-lookup"><span data-stu-id="22960-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="22960-104">Définit les paramètres relatifs aux conditions météorologiques de prévision d'un emplacement.</span><span class="sxs-lookup"><span data-stu-id="22960-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="22960-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="22960-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22960-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="22960-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="22960-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="22960-107">**Schema file**</span></span> <br/> |<span data-ttu-id="22960-108">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="22960-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="22960-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="22960-109">**Extension base**</span></span> <br/> |<span data-ttu-id="22960-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="22960-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="22960-111">Définition</span><span class="sxs-lookup"><span data-stu-id="22960-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="22960-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="22960-112">Elements and attributes</span></span>

<span data-ttu-id="22960-113">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="22960-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="22960-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="22960-114">Child elements</span></span>

<span data-ttu-id="22960-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="22960-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22960-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="22960-116">Attributes</span></span>

|<span data-ttu-id="22960-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="22960-117">**Attribute**</span></span>|<span data-ttu-id="22960-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="22960-118">**Type**</span></span>|<span data-ttu-id="22960-119">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="22960-119">**Required**</span></span>|<span data-ttu-id="22960-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="22960-120">**Description**</span></span>|<span data-ttu-id="22960-121">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="22960-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="22960-122">date</span><span class="sxs-lookup"><span data-stu-id="22960-122">date</span></span>  <br/> |<span data-ttu-id="22960-123">XS: date</span><span class="sxs-lookup"><span data-stu-id="22960-123">xs:date</span></span>  <br/> |<span data-ttu-id="22960-124">obligatoire</span><span class="sxs-lookup"><span data-stu-id="22960-124">required</span></span>  <br/> |<span data-ttu-id="22960-125">Indique la date de la prévision.</span><span class="sxs-lookup"><span data-stu-id="22960-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="22960-126">Une valeur de type xs: date</span><span class="sxs-lookup"><span data-stu-id="22960-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="22960-127">quotidienne</span><span class="sxs-lookup"><span data-stu-id="22960-127">day</span></span>  <br/> |<span data-ttu-id="22960-128">XS: String</span><span class="sxs-lookup"><span data-stu-id="22960-128">xs:string</span></span>  <br/> |<span data-ttu-id="22960-129">obligatoire</span><span class="sxs-lookup"><span data-stu-id="22960-129">required</span></span>  <br/> |<span data-ttu-id="22960-130">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="22960-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="22960-131">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="22960-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="22960-132">important</span><span class="sxs-lookup"><span data-stu-id="22960-132">high</span></span>  <br/> |<span data-ttu-id="22960-133">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="22960-133">xs:integer</span></span>  <br/> |<span data-ttu-id="22960-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="22960-134">required</span></span>  <br/> |<span data-ttu-id="22960-135">Spécifie la température la plus élevée prévue.</span><span class="sxs-lookup"><span data-stu-id="22960-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="22960-136">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="22960-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="22960-137">assez</span><span class="sxs-lookup"><span data-stu-id="22960-137">low</span></span>  <br/> |<span data-ttu-id="22960-138">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="22960-138">xs:integer</span></span>  <br/> |<span data-ttu-id="22960-139">obligatoire</span><span class="sxs-lookup"><span data-stu-id="22960-139">required</span></span>  <br/> |<span data-ttu-id="22960-140">Spécifie la température minimale prévue.</span><span class="sxs-lookup"><span data-stu-id="22960-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="22960-141">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="22960-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="22960-142">PRECIP</span><span class="sxs-lookup"><span data-stu-id="22960-142">precip</span></span>  <br/> |<span data-ttu-id="22960-143">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="22960-143">xs:integer</span></span>  <br/> |<span data-ttu-id="22960-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="22960-144">required</span></span>  <br/> |<span data-ttu-id="22960-145">Indique le pourcentage de probabilité de précipitation.</span><span class="sxs-lookup"><span data-stu-id="22960-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="22960-146">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="22960-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="22960-147">shortday</span><span class="sxs-lookup"><span data-stu-id="22960-147">shortday</span></span>  <br/> |<span data-ttu-id="22960-148">XS: String</span><span class="sxs-lookup"><span data-stu-id="22960-148">xs:string</span></span>  <br/> |<span data-ttu-id="22960-149">obligatoire</span><span class="sxs-lookup"><span data-stu-id="22960-149">required</span></span>  <br/> |<span data-ttu-id="22960-150">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="22960-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="22960-151">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="22960-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="22960-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="22960-152">skycodeday</span></span>  <br/> |<span data-ttu-id="22960-153">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="22960-153">xs:integer</span></span>  <br/> |<span data-ttu-id="22960-154">obligatoire</span><span class="sxs-lookup"><span data-stu-id="22960-154">required</span></span>  <br/> |<span data-ttu-id="22960-155">Spécifie un code pour les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="22960-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="22960-156">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="22960-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="22960-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="22960-157">skytextday</span></span>  <br/> |<span data-ttu-id="22960-158">XS: String</span><span class="sxs-lookup"><span data-stu-id="22960-158">xs:string</span></span>  <br/> |<span data-ttu-id="22960-159">obligatoire</span><span class="sxs-lookup"><span data-stu-id="22960-159">required</span></span>  <br/> |<span data-ttu-id="22960-160">Spécifie un à deux mots qui décrivent les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="22960-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="22960-161">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="22960-161">A value of the type xs:string</span></span>  <br/> |
   

