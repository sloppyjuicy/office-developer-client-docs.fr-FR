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
ms.openlocfilehash: 55ea2cfa6904d88c695268675bc7a893fa643010
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787719"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="99ef9-103">type complexe currentType (schéma des informations météo Outlook)</span><span class="sxs-lookup"><span data-stu-id="99ef9-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="99ef9-104">Définit les paramètres sur la météo d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="99ef9-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="99ef9-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="99ef9-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99ef9-106">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="99ef9-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="99ef9-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="99ef9-107">**Schema file**</span></span> <br/> |<span data-ttu-id="99ef9-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="99ef9-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="99ef9-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="99ef9-109">**Extension base**</span></span> <br/> |<span data-ttu-id="99ef9-110">Aucune</span><span class="sxs-lookup"><span data-stu-id="99ef9-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="99ef9-111">Définition</span><span class="sxs-lookup"><span data-stu-id="99ef9-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="99ef9-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="99ef9-112">Elements and attributes</span></span>

<span data-ttu-id="99ef9-113">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="99ef9-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="99ef9-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="99ef9-114">Child elements</span></span>

<span data-ttu-id="99ef9-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="99ef9-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99ef9-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="99ef9-116">Attributes</span></span>

|<span data-ttu-id="99ef9-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="99ef9-117">**Attribute**</span></span>|<span data-ttu-id="99ef9-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="99ef9-118">**Type**</span></span>|<span data-ttu-id="99ef9-119">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="99ef9-119">**Required**</span></span>|<span data-ttu-id="99ef9-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="99ef9-120">**Description**</span></span>|<span data-ttu-id="99ef9-121">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="99ef9-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="99ef9-122">date</span><span class="sxs-lookup"><span data-stu-id="99ef9-122">date</span></span>  <br/> |<span data-ttu-id="99ef9-123">xs : date</span><span class="sxs-lookup"><span data-stu-id="99ef9-123">xs:date</span></span>  <br/> |<span data-ttu-id="99ef9-124">obligatoire</span><span class="sxs-lookup"><span data-stu-id="99ef9-124">required</span></span>  <br/> |<span data-ttu-id="99ef9-125">Spécifie la date du jour.</span><span class="sxs-lookup"><span data-stu-id="99ef9-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="99ef9-126">Valeur du type xs : date</span><span class="sxs-lookup"><span data-stu-id="99ef9-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="99ef9-127">jour</span><span class="sxs-lookup"><span data-stu-id="99ef9-127">day</span></span>  <br/> |<span data-ttu-id="99ef9-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="99ef9-128">xs:string</span></span>  <br/> |<span data-ttu-id="99ef9-129">facultatif</span><span class="sxs-lookup"><span data-stu-id="99ef9-129">optional</span></span>  <br/> |<span data-ttu-id="99ef9-130">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="99ef9-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="99ef9-131">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="99ef9-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="99ef9-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="99ef9-132">feelslike</span></span>  <br/> |<span data-ttu-id="99ef9-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="99ef9-133">xs:integer</span></span>  <br/> |<span data-ttu-id="99ef9-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="99ef9-134">required</span></span>  <br/> |<span data-ttu-id="99ef9-135">Spécifie comment la météo actuelle semble la température.</span><span class="sxs-lookup"><span data-stu-id="99ef9-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="99ef9-136">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="99ef9-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="99ef9-137">humidité</span><span class="sxs-lookup"><span data-stu-id="99ef9-137">humidity</span></span>  <br/> |<span data-ttu-id="99ef9-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="99ef9-138">xs:integer</span></span>  <br/> |<span data-ttu-id="99ef9-139">obligatoire</span><span class="sxs-lookup"><span data-stu-id="99ef9-139">required</span></span>  <br/> |<span data-ttu-id="99ef9-140">Spécifie la valeur numérique humidité actuel.</span><span class="sxs-lookup"><span data-stu-id="99ef9-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="99ef9-141">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="99ef9-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="99ef9-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="99ef9-142">observationpoint</span></span>  <br/> |<span data-ttu-id="99ef9-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="99ef9-143">xs:string</span></span>  <br/> |<span data-ttu-id="99ef9-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="99ef9-144">required</span></span>  <br/> |<span data-ttu-id="99ef9-145">Spécifie où la météo actuelle est observée à partir.</span><span class="sxs-lookup"><span data-stu-id="99ef9-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="99ef9-146">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="99ef9-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="99ef9-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="99ef9-147">observationtime</span></span>  <br/> |<span data-ttu-id="99ef9-148">xs : Time</span><span class="sxs-lookup"><span data-stu-id="99ef9-148">xs:time</span></span>  <br/> |<span data-ttu-id="99ef9-149">obligatoire</span><span class="sxs-lookup"><span data-stu-id="99ef9-149">required</span></span>  <br/> |<span data-ttu-id="99ef9-150">Spécifie que lorsque la météo actuelle est observée à.</span><span class="sxs-lookup"><span data-stu-id="99ef9-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="99ef9-151">Une valeur de la xs : time type</span><span class="sxs-lookup"><span data-stu-id="99ef9-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="99ef9-152">shortday</span><span class="sxs-lookup"><span data-stu-id="99ef9-152">shortday</span></span>  <br/> |<span data-ttu-id="99ef9-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="99ef9-153">xs:string</span></span>  <br/> |<span data-ttu-id="99ef9-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="99ef9-154">optional</span></span>  <br/> |<span data-ttu-id="99ef9-155">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="99ef9-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="99ef9-156">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="99ef9-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="99ef9-157">skycode</span><span class="sxs-lookup"><span data-stu-id="99ef9-157">skycode</span></span>  <br/> |<span data-ttu-id="99ef9-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="99ef9-158">xs:integer</span></span>  <br/> |<span data-ttu-id="99ef9-159">obligatoire</span><span class="sxs-lookup"><span data-stu-id="99ef9-159">required</span></span>  <br/> |<span data-ttu-id="99ef9-160">Spécifie un code de type entier pour la météo.</span><span class="sxs-lookup"><span data-stu-id="99ef9-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="99ef9-161">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="99ef9-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="99ef9-162">skytext</span><span class="sxs-lookup"><span data-stu-id="99ef9-162">skytext</span></span>  <br/> |<span data-ttu-id="99ef9-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="99ef9-163">xs:string</span></span>  <br/> |<span data-ttu-id="99ef9-164">obligatoire</span><span class="sxs-lookup"><span data-stu-id="99ef9-164">required</span></span>  <br/> |<span data-ttu-id="99ef9-165">Spécifie un ou deux mots décrivant la météo.</span><span class="sxs-lookup"><span data-stu-id="99ef9-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="99ef9-166">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="99ef9-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="99ef9-167">température</span><span class="sxs-lookup"><span data-stu-id="99ef9-167">temperature</span></span>  <br/> |<span data-ttu-id="99ef9-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="99ef9-168">xs:integer</span></span>  <br/> |<span data-ttu-id="99ef9-169">obligatoire</span><span class="sxs-lookup"><span data-stu-id="99ef9-169">required</span></span>  <br/> |<span data-ttu-id="99ef9-170">Spécifie la température de l’emplacement actuelle.</span><span class="sxs-lookup"><span data-stu-id="99ef9-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="99ef9-171">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="99ef9-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="99ef9-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="99ef9-172">winddisplay</span></span>  <br/> |<span data-ttu-id="99ef9-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="99ef9-173">xs:string</span></span>  <br/> |<span data-ttu-id="99ef9-174">obligatoire</span><span class="sxs-lookup"><span data-stu-id="99ef9-174">required</span></span>  <br/> |<span data-ttu-id="99ef9-175">Chaîne qui décrit les conditions de vent en cours.</span><span class="sxs-lookup"><span data-stu-id="99ef9-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="99ef9-176">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="99ef9-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="99ef9-177">vitesse du vent</span><span class="sxs-lookup"><span data-stu-id="99ef9-177">windspeed</span></span>  <br/> |<span data-ttu-id="99ef9-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="99ef9-178">xs:integer</span></span>  <br/> |<span data-ttu-id="99ef9-179">obligatoire</span><span class="sxs-lookup"><span data-stu-id="99ef9-179">required</span></span>  <br/> |<span data-ttu-id="99ef9-180">Spécifie la valeur actuelle de la vitesse vent numérique.</span><span class="sxs-lookup"><span data-stu-id="99ef9-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="99ef9-181">Une valeur de la xs : Integer type</span><span class="sxs-lookup"><span data-stu-id="99ef9-181">A value of the type xs:integer</span></span>  <br/> |
   

