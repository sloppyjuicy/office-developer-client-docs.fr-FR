---
title: complexType currentType (schéma d’informations météorologiques Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Définit les paramètres relatifs aux conditions météorologiques actuelles d’un emplacement.
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540986"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="7f26c-103">complexType currentType (schéma d’informations météorologiques Outlook)</span><span class="sxs-lookup"><span data-stu-id="7f26c-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="7f26c-104">Définit les paramètres relatifs aux conditions météorologiques actuelles d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="7f26c-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="7f26c-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7f26c-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f26c-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7f26c-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="7f26c-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7f26c-107">**Schema file**</span></span> <br/> |<span data-ttu-id="7f26c-108">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="7f26c-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="7f26c-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7f26c-109">**Extension base**</span></span> <br/> |<span data-ttu-id="7f26c-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="7f26c-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7f26c-111">Définition</span><span class="sxs-lookup"><span data-stu-id="7f26c-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7f26c-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7f26c-112">Elements and attributes</span></span>

<span data-ttu-id="7f26c-113">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="7f26c-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7f26c-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7f26c-114">Child elements</span></span>

<span data-ttu-id="7f26c-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7f26c-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f26c-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="7f26c-116">Attributes</span></span>

|<span data-ttu-id="7f26c-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7f26c-117">**Attribute**</span></span>|<span data-ttu-id="7f26c-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="7f26c-118">**Type**</span></span>|<span data-ttu-id="7f26c-119">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="7f26c-119">**Required**</span></span>|<span data-ttu-id="7f26c-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="7f26c-120">**Description**</span></span>|<span data-ttu-id="7f26c-121">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="7f26c-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7f26c-122">date</span><span class="sxs-lookup"><span data-stu-id="7f26c-122">date</span></span>  <br/> |<span data-ttu-id="7f26c-123">XS: date</span><span class="sxs-lookup"><span data-stu-id="7f26c-123">xs:date</span></span>  <br/> |<span data-ttu-id="7f26c-124">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f26c-124">required</span></span>  <br/> |<span data-ttu-id="7f26c-125">Indique la date du jour.</span><span class="sxs-lookup"><span data-stu-id="7f26c-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="7f26c-126">Une valeur de type xs: date</span><span class="sxs-lookup"><span data-stu-id="7f26c-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="7f26c-127">quotidienne</span><span class="sxs-lookup"><span data-stu-id="7f26c-127">day</span></span>  <br/> |<span data-ttu-id="7f26c-128">XS: String</span><span class="sxs-lookup"><span data-stu-id="7f26c-128">xs:string</span></span>  <br/> |<span data-ttu-id="7f26c-129">facultatif</span><span class="sxs-lookup"><span data-stu-id="7f26c-129">optional</span></span>  <br/> |<span data-ttu-id="7f26c-130">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="7f26c-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="7f26c-131">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="7f26c-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7f26c-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="7f26c-132">feelslike</span></span>  <br/> |<span data-ttu-id="7f26c-133">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="7f26c-133">xs:integer</span></span>  <br/> |<span data-ttu-id="7f26c-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f26c-134">required</span></span>  <br/> |<span data-ttu-id="7f26c-135">Indique la température de la météo actuelle.</span><span class="sxs-lookup"><span data-stu-id="7f26c-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="7f26c-136">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="7f26c-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="7f26c-137">Humid</span><span class="sxs-lookup"><span data-stu-id="7f26c-137">humidity</span></span>  <br/> |<span data-ttu-id="7f26c-138">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="7f26c-138">xs:integer</span></span>  <br/> |<span data-ttu-id="7f26c-139">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f26c-139">required</span></span>  <br/> |<span data-ttu-id="7f26c-140">Indique la valeur d’humidité numérique actuelle.</span><span class="sxs-lookup"><span data-stu-id="7f26c-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="7f26c-141">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="7f26c-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="7f26c-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="7f26c-142">observationpoint</span></span>  <br/> |<span data-ttu-id="7f26c-143">XS: String</span><span class="sxs-lookup"><span data-stu-id="7f26c-143">xs:string</span></span>  <br/> |<span data-ttu-id="7f26c-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f26c-144">required</span></span>  <br/> |<span data-ttu-id="7f26c-145">Spécifie l’emplacement à partir duquel les informations météorologiques actuelles sont observées.</span><span class="sxs-lookup"><span data-stu-id="7f26c-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="7f26c-146">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="7f26c-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7f26c-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="7f26c-147">observationtime</span></span>  <br/> |<span data-ttu-id="7f26c-148">XS: Time</span><span class="sxs-lookup"><span data-stu-id="7f26c-148">xs:time</span></span>  <br/> |<span data-ttu-id="7f26c-149">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f26c-149">required</span></span>  <br/> |<span data-ttu-id="7f26c-150">Indique quand les informations météorologiques actuelles sont observées à.</span><span class="sxs-lookup"><span data-stu-id="7f26c-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="7f26c-151">Une valeur du type xs: Time</span><span class="sxs-lookup"><span data-stu-id="7f26c-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="7f26c-152">shortday</span><span class="sxs-lookup"><span data-stu-id="7f26c-152">shortday</span></span>  <br/> |<span data-ttu-id="7f26c-153">XS: String</span><span class="sxs-lookup"><span data-stu-id="7f26c-153">xs:string</span></span>  <br/> |<span data-ttu-id="7f26c-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="7f26c-154">optional</span></span>  <br/> |<span data-ttu-id="7f26c-155">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="7f26c-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="7f26c-156">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="7f26c-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7f26c-157">skycode</span><span class="sxs-lookup"><span data-stu-id="7f26c-157">skycode</span></span>  <br/> |<span data-ttu-id="7f26c-158">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="7f26c-158">xs:integer</span></span>  <br/> |<span data-ttu-id="7f26c-159">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f26c-159">required</span></span>  <br/> |<span data-ttu-id="7f26c-160">Spécifie un code entier pour les conditions météorologiques actuelles.</span><span class="sxs-lookup"><span data-stu-id="7f26c-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="7f26c-161">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="7f26c-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="7f26c-162">skytext</span><span class="sxs-lookup"><span data-stu-id="7f26c-162">skytext</span></span>  <br/> |<span data-ttu-id="7f26c-163">XS: String</span><span class="sxs-lookup"><span data-stu-id="7f26c-163">xs:string</span></span>  <br/> |<span data-ttu-id="7f26c-164">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f26c-164">required</span></span>  <br/> |<span data-ttu-id="7f26c-165">Spécifie un à deux mots qui décrivent les conditions météorologiques actuelles.</span><span class="sxs-lookup"><span data-stu-id="7f26c-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="7f26c-166">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="7f26c-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7f26c-167">régulation</span><span class="sxs-lookup"><span data-stu-id="7f26c-167">temperature</span></span>  <br/> |<span data-ttu-id="7f26c-168">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="7f26c-168">xs:integer</span></span>  <br/> |<span data-ttu-id="7f26c-169">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f26c-169">required</span></span>  <br/> |<span data-ttu-id="7f26c-170">Indique la température actuelle de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="7f26c-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="7f26c-171">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="7f26c-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="7f26c-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="7f26c-172">winddisplay</span></span>  <br/> |<span data-ttu-id="7f26c-173">XS: String</span><span class="sxs-lookup"><span data-stu-id="7f26c-173">xs:string</span></span>  <br/> |<span data-ttu-id="7f26c-174">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f26c-174">required</span></span>  <br/> |<span data-ttu-id="7f26c-175">Chaîne qui décrit les conditions de vent actuelles.</span><span class="sxs-lookup"><span data-stu-id="7f26c-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="7f26c-176">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="7f26c-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="7f26c-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="7f26c-177">windspeed</span></span>  <br/> |<span data-ttu-id="7f26c-178">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="7f26c-178">xs:integer</span></span>  <br/> |<span data-ttu-id="7f26c-179">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f26c-179">required</span></span>  <br/> |<span data-ttu-id="7f26c-180">Spécifie la valeur numérique de la vitesse du vent.</span><span class="sxs-lookup"><span data-stu-id="7f26c-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="7f26c-181">Valeur de type xs: Integer</span><span class="sxs-lookup"><span data-stu-id="7f26c-181">A value of the type xs:integer</span></span>  <br/> |
   

