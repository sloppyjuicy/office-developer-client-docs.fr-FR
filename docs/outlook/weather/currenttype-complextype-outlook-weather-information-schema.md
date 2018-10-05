---
title: type complexe currentType (schéma des informations météo Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Définit les paramètres sur la météo d’un emplacement.
ms.openlocfilehash: 16d3e23375f68315c9b9f3a7e914d93f4fec9d0a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387033"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="62a5c-103">type complexe currentType (schéma des informations météo Outlook)</span><span class="sxs-lookup"><span data-stu-id="62a5c-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="62a5c-104">Définit les paramètres sur la météo d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="62a5c-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="62a5c-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="62a5c-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62a5c-106">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="62a5c-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="62a5c-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="62a5c-107">**Schema file**</span></span> <br/> |<span data-ttu-id="62a5c-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="62a5c-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="62a5c-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="62a5c-109">**Extension base**</span></span> <br/> |<span data-ttu-id="62a5c-110">Aucune</span><span class="sxs-lookup"><span data-stu-id="62a5c-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62a5c-111">Définition</span><span class="sxs-lookup"><span data-stu-id="62a5c-111">Definition</span></span>

```XML
       <xs:complexType name="currentType">
     <xs:attribute name="winddisplay"   type="xs:string"      use="required"     />
     <xs:attribute name="windspeed"   type="xs:integer"      use="required"     />
     <xs:attribute name="humidity"   type="xs:integer"      use="required"     />
     <xs:attribute name="feelslike"   type="xs:integer"      use="required"     />
     <xs:attribute name="observationpoint"   type="xs:string"      use="required"     />
     <xs:attribute name="observationtime"   type="xs:time"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="skytext"   type="xs:string"      use="required"     />
     <xs:attribute name="skycode"   type="xs:integer"      use="required"     />
     <xs:attribute name="temperature"   type="xs:integer"      use="required"     />
     <xs:attribute name="shortday"   type="xs:string"      use="optional"     />
     <xs:attribute name="day"   type="xs:string"      use="optional"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="62a5c-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="62a5c-112">Elements and attributes</span></span>

<span data-ttu-id="62a5c-113">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="62a5c-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="62a5c-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="62a5c-114">Child elements</span></span>

<span data-ttu-id="62a5c-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="62a5c-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62a5c-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="62a5c-116">Attributes</span></span>

|<span data-ttu-id="62a5c-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="62a5c-117">**Attribute**</span></span>|<span data-ttu-id="62a5c-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="62a5c-118">**Type**</span></span>|<span data-ttu-id="62a5c-119">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="62a5c-119">**Required**</span></span>|<span data-ttu-id="62a5c-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="62a5c-120">**Description**</span></span>|<span data-ttu-id="62a5c-121">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="62a5c-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="62a5c-122">date</span><span class="sxs-lookup"><span data-stu-id="62a5c-122">date</span></span>  <br/> |<span data-ttu-id="62a5c-123">xs : date</span><span class="sxs-lookup"><span data-stu-id="62a5c-123">xs:date</span></span>  <br/> |<span data-ttu-id="62a5c-124">obligatoire</span><span class="sxs-lookup"><span data-stu-id="62a5c-124">required</span></span>  <br/> |<span data-ttu-id="62a5c-125">Spécifie la date du jour.</span><span class="sxs-lookup"><span data-stu-id="62a5c-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="62a5c-126">Valeur du type xs : date</span><span class="sxs-lookup"><span data-stu-id="62a5c-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="62a5c-127">jour</span><span class="sxs-lookup"><span data-stu-id="62a5c-127">day</span></span>  <br/> |<span data-ttu-id="62a5c-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="62a5c-128">xs:string</span></span>  <br/> |<span data-ttu-id="62a5c-129">facultatif</span><span class="sxs-lookup"><span data-stu-id="62a5c-129">optional</span></span>  <br/> |<span data-ttu-id="62a5c-130">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="62a5c-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="62a5c-131">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="62a5c-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="62a5c-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="62a5c-132">feelslike</span></span>  <br/> |<span data-ttu-id="62a5c-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="62a5c-133">xs:integer</span></span>  <br/> |<span data-ttu-id="62a5c-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="62a5c-134">required</span></span>  <br/> |<span data-ttu-id="62a5c-135">Spécifie comment la météo actuelle semble la température.</span><span class="sxs-lookup"><span data-stu-id="62a5c-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="62a5c-136">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="62a5c-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="62a5c-137">humidité</span><span class="sxs-lookup"><span data-stu-id="62a5c-137">humidity</span></span>  <br/> |<span data-ttu-id="62a5c-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="62a5c-138">xs:integer</span></span>  <br/> |<span data-ttu-id="62a5c-139">obligatoire</span><span class="sxs-lookup"><span data-stu-id="62a5c-139">required</span></span>  <br/> |<span data-ttu-id="62a5c-140">Spécifie la valeur numérique humidité actuel.</span><span class="sxs-lookup"><span data-stu-id="62a5c-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="62a5c-141">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="62a5c-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="62a5c-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="62a5c-142">observationpoint</span></span>  <br/> |<span data-ttu-id="62a5c-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="62a5c-143">xs:string</span></span>  <br/> |<span data-ttu-id="62a5c-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="62a5c-144">required</span></span>  <br/> |<span data-ttu-id="62a5c-145">Spécifie où la météo actuelle est observée à partir.</span><span class="sxs-lookup"><span data-stu-id="62a5c-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="62a5c-146">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="62a5c-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="62a5c-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="62a5c-147">observationtime</span></span>  <br/> |<span data-ttu-id="62a5c-148">xs : Time</span><span class="sxs-lookup"><span data-stu-id="62a5c-148">xs:time</span></span>  <br/> |<span data-ttu-id="62a5c-149">obligatoire</span><span class="sxs-lookup"><span data-stu-id="62a5c-149">required</span></span>  <br/> |<span data-ttu-id="62a5c-150">Spécifie que lorsque la météo actuelle est observée à.</span><span class="sxs-lookup"><span data-stu-id="62a5c-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="62a5c-151">Une valeur de la xs : time type</span><span class="sxs-lookup"><span data-stu-id="62a5c-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="62a5c-152">shortday</span><span class="sxs-lookup"><span data-stu-id="62a5c-152">shortday</span></span>  <br/> |<span data-ttu-id="62a5c-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="62a5c-153">xs:string</span></span>  <br/> |<span data-ttu-id="62a5c-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="62a5c-154">optional</span></span>  <br/> |<span data-ttu-id="62a5c-155">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="62a5c-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="62a5c-156">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="62a5c-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="62a5c-157">skycode</span><span class="sxs-lookup"><span data-stu-id="62a5c-157">skycode</span></span>  <br/> |<span data-ttu-id="62a5c-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="62a5c-158">xs:integer</span></span>  <br/> |<span data-ttu-id="62a5c-159">obligatoire</span><span class="sxs-lookup"><span data-stu-id="62a5c-159">required</span></span>  <br/> |<span data-ttu-id="62a5c-160">Spécifie un code de type entier pour la météo.</span><span class="sxs-lookup"><span data-stu-id="62a5c-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="62a5c-161">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="62a5c-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="62a5c-162">skytext</span><span class="sxs-lookup"><span data-stu-id="62a5c-162">skytext</span></span>  <br/> |<span data-ttu-id="62a5c-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="62a5c-163">xs:string</span></span>  <br/> |<span data-ttu-id="62a5c-164">obligatoire</span><span class="sxs-lookup"><span data-stu-id="62a5c-164">required</span></span>  <br/> |<span data-ttu-id="62a5c-165">Spécifie un ou deux mots décrivant la météo.</span><span class="sxs-lookup"><span data-stu-id="62a5c-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="62a5c-166">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="62a5c-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="62a5c-167">température</span><span class="sxs-lookup"><span data-stu-id="62a5c-167">temperature</span></span>  <br/> |<span data-ttu-id="62a5c-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="62a5c-168">xs:integer</span></span>  <br/> |<span data-ttu-id="62a5c-169">obligatoire</span><span class="sxs-lookup"><span data-stu-id="62a5c-169">required</span></span>  <br/> |<span data-ttu-id="62a5c-170">Spécifie la température de l’emplacement actuelle.</span><span class="sxs-lookup"><span data-stu-id="62a5c-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="62a5c-171">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="62a5c-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="62a5c-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="62a5c-172">winddisplay</span></span>  <br/> |<span data-ttu-id="62a5c-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="62a5c-173">xs:string</span></span>  <br/> |<span data-ttu-id="62a5c-174">obligatoire</span><span class="sxs-lookup"><span data-stu-id="62a5c-174">required</span></span>  <br/> |<span data-ttu-id="62a5c-175">Chaîne qui décrit les conditions de vent en cours.</span><span class="sxs-lookup"><span data-stu-id="62a5c-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="62a5c-176">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="62a5c-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="62a5c-177">vitesse du vent</span><span class="sxs-lookup"><span data-stu-id="62a5c-177">windspeed</span></span>  <br/> |<span data-ttu-id="62a5c-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="62a5c-178">xs:integer</span></span>  <br/> |<span data-ttu-id="62a5c-179">obligatoire</span><span class="sxs-lookup"><span data-stu-id="62a5c-179">required</span></span>  <br/> |<span data-ttu-id="62a5c-180">Spécifie la valeur actuelle de la vitesse vent numérique.</span><span class="sxs-lookup"><span data-stu-id="62a5c-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="62a5c-181">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="62a5c-181">A value of the type xs:integer</span></span>  <br/> |
   

