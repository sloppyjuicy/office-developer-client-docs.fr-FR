---
title: forecastType complexType (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Définit les paramètres des prévisions météorologiques d’un emplacement.
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540951"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="4afc7-103">forecastType complexType (Outlook Weather Information Schema)</span><span class="sxs-lookup"><span data-stu-id="4afc7-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="4afc7-104">Définit les paramètres des prévisions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="4afc7-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="4afc7-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="4afc7-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4afc7-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4afc7-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="4afc7-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4afc7-107">**Schema file**</span></span> <br/> |<span data-ttu-id="4afc7-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="4afc7-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="4afc7-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="4afc7-109">**Extension base**</span></span> <br/> |<span data-ttu-id="4afc7-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="4afc7-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4afc7-111">Définition</span><span class="sxs-lookup"><span data-stu-id="4afc7-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4afc7-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4afc7-112">Elements and attributes</span></span>

<span data-ttu-id="4afc7-113">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="4afc7-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4afc7-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4afc7-114">Child elements</span></span>

<span data-ttu-id="4afc7-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4afc7-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4afc7-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="4afc7-116">Attributes</span></span>

|<span data-ttu-id="4afc7-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4afc7-117">**Attribute**</span></span>|<span data-ttu-id="4afc7-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="4afc7-118">**Type**</span></span>|<span data-ttu-id="4afc7-119">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4afc7-119">**Required**</span></span>|<span data-ttu-id="4afc7-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="4afc7-120">**Description**</span></span>|<span data-ttu-id="4afc7-121">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4afc7-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4afc7-122">date</span><span class="sxs-lookup"><span data-stu-id="4afc7-122">date</span></span>  <br/> |<span data-ttu-id="4afc7-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="4afc7-123">xs:date</span></span>  <br/> |<span data-ttu-id="4afc7-124">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4afc7-124">required</span></span>  <br/> |<span data-ttu-id="4afc7-125">Spécifie la date de la prévision.</span><span class="sxs-lookup"><span data-stu-id="4afc7-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="4afc7-126">Valeur du type xs:date</span><span class="sxs-lookup"><span data-stu-id="4afc7-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="4afc7-127">day</span><span class="sxs-lookup"><span data-stu-id="4afc7-127">day</span></span>  <br/> |<span data-ttu-id="4afc7-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="4afc7-128">xs:string</span></span>  <br/> |<span data-ttu-id="4afc7-129">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4afc7-129">required</span></span>  <br/> |<span data-ttu-id="4afc7-130">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="4afc7-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="4afc7-131">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="4afc7-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4afc7-132">high</span><span class="sxs-lookup"><span data-stu-id="4afc7-132">high</span></span>  <br/> |<span data-ttu-id="4afc7-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4afc7-133">xs:integer</span></span>  <br/> |<span data-ttu-id="4afc7-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4afc7-134">required</span></span>  <br/> |<span data-ttu-id="4afc7-135">Spécifie la température la plus élevée prévue.</span><span class="sxs-lookup"><span data-stu-id="4afc7-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="4afc7-136">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="4afc7-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4afc7-137">low</span><span class="sxs-lookup"><span data-stu-id="4afc7-137">low</span></span>  <br/> |<span data-ttu-id="4afc7-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4afc7-138">xs:integer</span></span>  <br/> |<span data-ttu-id="4afc7-139">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4afc7-139">required</span></span>  <br/> |<span data-ttu-id="4afc7-140">Spécifie la température la plus basse prévue.</span><span class="sxs-lookup"><span data-stu-id="4afc7-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="4afc7-141">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="4afc7-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4afc7-142">precip</span><span class="sxs-lookup"><span data-stu-id="4afc7-142">precip</span></span>  <br/> |<span data-ttu-id="4afc7-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4afc7-143">xs:integer</span></span>  <br/> |<span data-ttu-id="4afc7-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4afc7-144">required</span></span>  <br/> |<span data-ttu-id="4afc7-145">Spécifie la possibilité de pourcentage d’éventualité.</span><span class="sxs-lookup"><span data-stu-id="4afc7-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="4afc7-146">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="4afc7-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4afc7-147">shortday</span><span class="sxs-lookup"><span data-stu-id="4afc7-147">shortday</span></span>  <br/> |<span data-ttu-id="4afc7-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="4afc7-148">xs:string</span></span>  <br/> |<span data-ttu-id="4afc7-149">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4afc7-149">required</span></span>  <br/> |<span data-ttu-id="4afc7-150">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="4afc7-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="4afc7-151">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="4afc7-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4afc7-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="4afc7-152">skycodeday</span></span>  <br/> |<span data-ttu-id="4afc7-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4afc7-153">xs:integer</span></span>  <br/> |<span data-ttu-id="4afc7-154">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4afc7-154">required</span></span>  <br/> |<span data-ttu-id="4afc7-155">Spécifie un code pour les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="4afc7-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="4afc7-156">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="4afc7-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4afc7-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="4afc7-157">skytextday</span></span>  <br/> |<span data-ttu-id="4afc7-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="4afc7-158">xs:string</span></span>  <br/> |<span data-ttu-id="4afc7-159">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4afc7-159">required</span></span>  <br/> |<span data-ttu-id="4afc7-160">Spécifie un à deux mots qui décrivent les conditions prévues.</span><span class="sxs-lookup"><span data-stu-id="4afc7-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="4afc7-161">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="4afc7-161">A value of the type xs:string</span></span>  <br/> |
   

