---
title: complexType currentType (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Définit les paramètres sur les conditions météorologiques actuelles d’un emplacement.
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540986"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="cbb51-103">complexType currentType (Outlook Weather Information Schema)</span><span class="sxs-lookup"><span data-stu-id="cbb51-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="cbb51-104">Définit les paramètres sur les conditions météorologiques actuelles d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="cbb51-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="cbb51-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="cbb51-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbb51-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cbb51-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="cbb51-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="cbb51-107">**Schema file**</span></span> <br/> |<span data-ttu-id="cbb51-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="cbb51-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="cbb51-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="cbb51-109">**Extension base**</span></span> <br/> |<span data-ttu-id="cbb51-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="cbb51-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cbb51-111">Définition</span><span class="sxs-lookup"><span data-stu-id="cbb51-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cbb51-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="cbb51-112">Elements and attributes</span></span>

<span data-ttu-id="cbb51-113">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="cbb51-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cbb51-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cbb51-114">Child elements</span></span>

<span data-ttu-id="cbb51-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cbb51-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbb51-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="cbb51-116">Attributes</span></span>

|<span data-ttu-id="cbb51-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cbb51-117">**Attribute**</span></span>|<span data-ttu-id="cbb51-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="cbb51-118">**Type**</span></span>|<span data-ttu-id="cbb51-119">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="cbb51-119">**Required**</span></span>|<span data-ttu-id="cbb51-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="cbb51-120">**Description**</span></span>|<span data-ttu-id="cbb51-121">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="cbb51-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cbb51-122">date</span><span class="sxs-lookup"><span data-stu-id="cbb51-122">date</span></span>  <br/> |<span data-ttu-id="cbb51-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="cbb51-123">xs:date</span></span>  <br/> |<span data-ttu-id="cbb51-124">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cbb51-124">required</span></span>  <br/> |<span data-ttu-id="cbb51-125">Spécifie la date du jour.</span><span class="sxs-lookup"><span data-stu-id="cbb51-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="cbb51-126">Valeur du type xs:date</span><span class="sxs-lookup"><span data-stu-id="cbb51-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="cbb51-127">day</span><span class="sxs-lookup"><span data-stu-id="cbb51-127">day</span></span>  <br/> |<span data-ttu-id="cbb51-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="cbb51-128">xs:string</span></span>  <br/> |<span data-ttu-id="cbb51-129">facultatif</span><span class="sxs-lookup"><span data-stu-id="cbb51-129">optional</span></span>  <br/> |<span data-ttu-id="cbb51-130">Spécifie un jour pour la prévision.</span><span class="sxs-lookup"><span data-stu-id="cbb51-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="cbb51-131">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="cbb51-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cbb51-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="cbb51-132">feelslike</span></span>  <br/> |<span data-ttu-id="cbb51-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cbb51-133">xs:integer</span></span>  <br/> |<span data-ttu-id="cbb51-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cbb51-134">required</span></span>  <br/> |<span data-ttu-id="cbb51-135">Spécifie la température de la météo actuelle.</span><span class="sxs-lookup"><span data-stu-id="cbb51-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="cbb51-136">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="cbb51-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="cbb51-137">humidité</span><span class="sxs-lookup"><span data-stu-id="cbb51-137">humidity</span></span>  <br/> |<span data-ttu-id="cbb51-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cbb51-138">xs:integer</span></span>  <br/> |<span data-ttu-id="cbb51-139">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cbb51-139">required</span></span>  <br/> |<span data-ttu-id="cbb51-140">Spécifie la valeur d’humidité numérique actuelle.</span><span class="sxs-lookup"><span data-stu-id="cbb51-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="cbb51-141">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="cbb51-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="cbb51-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="cbb51-142">observationpoint</span></span>  <br/> |<span data-ttu-id="cbb51-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="cbb51-143">xs:string</span></span>  <br/> |<span data-ttu-id="cbb51-144">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cbb51-144">required</span></span>  <br/> |<span data-ttu-id="cbb51-145">Spécifie d’où les informations météorologiques actuelles sont observées.</span><span class="sxs-lookup"><span data-stu-id="cbb51-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="cbb51-146">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="cbb51-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cbb51-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="cbb51-147">observationtime</span></span>  <br/> |<span data-ttu-id="cbb51-148">xs:time</span><span class="sxs-lookup"><span data-stu-id="cbb51-148">xs:time</span></span>  <br/> |<span data-ttu-id="cbb51-149">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cbb51-149">required</span></span>  <br/> |<span data-ttu-id="cbb51-150">Indique à quel moment les informations météorologiques actuelles sont observées.</span><span class="sxs-lookup"><span data-stu-id="cbb51-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="cbb51-151">Valeur du type xs:time</span><span class="sxs-lookup"><span data-stu-id="cbb51-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="cbb51-152">shortday</span><span class="sxs-lookup"><span data-stu-id="cbb51-152">shortday</span></span>  <br/> |<span data-ttu-id="cbb51-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="cbb51-153">xs:string</span></span>  <br/> |<span data-ttu-id="cbb51-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="cbb51-154">optional</span></span>  <br/> |<span data-ttu-id="cbb51-155">Spécifie un jour sous forme abrégée.</span><span class="sxs-lookup"><span data-stu-id="cbb51-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="cbb51-156">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="cbb51-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cbb51-157">skycode</span><span class="sxs-lookup"><span data-stu-id="cbb51-157">skycode</span></span>  <br/> |<span data-ttu-id="cbb51-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cbb51-158">xs:integer</span></span>  <br/> |<span data-ttu-id="cbb51-159">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cbb51-159">required</span></span>  <br/> |<span data-ttu-id="cbb51-160">Spécifie un code d’un nombre integer pour les conditions météorologiques actuelles.</span><span class="sxs-lookup"><span data-stu-id="cbb51-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="cbb51-161">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="cbb51-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="cbb51-162">skytext</span><span class="sxs-lookup"><span data-stu-id="cbb51-162">skytext</span></span>  <br/> |<span data-ttu-id="cbb51-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="cbb51-163">xs:string</span></span>  <br/> |<span data-ttu-id="cbb51-164">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cbb51-164">required</span></span>  <br/> |<span data-ttu-id="cbb51-165">Spécifie un à deux mots décrivant les conditions météorologiques actuelles.</span><span class="sxs-lookup"><span data-stu-id="cbb51-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="cbb51-166">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="cbb51-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cbb51-167">température</span><span class="sxs-lookup"><span data-stu-id="cbb51-167">temperature</span></span>  <br/> |<span data-ttu-id="cbb51-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cbb51-168">xs:integer</span></span>  <br/> |<span data-ttu-id="cbb51-169">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cbb51-169">required</span></span>  <br/> |<span data-ttu-id="cbb51-170">Spécifie la température actuelle de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="cbb51-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="cbb51-171">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="cbb51-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="cbb51-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="cbb51-172">winddisplay</span></span>  <br/> |<span data-ttu-id="cbb51-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="cbb51-173">xs:string</span></span>  <br/> |<span data-ttu-id="cbb51-174">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cbb51-174">required</span></span>  <br/> |<span data-ttu-id="cbb51-175">Chaîne qui décrit les conditions actuelles du vent.</span><span class="sxs-lookup"><span data-stu-id="cbb51-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="cbb51-176">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="cbb51-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="cbb51-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="cbb51-177">windspeed</span></span>  <br/> |<span data-ttu-id="cbb51-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="cbb51-178">xs:integer</span></span>  <br/> |<span data-ttu-id="cbb51-179">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cbb51-179">required</span></span>  <br/> |<span data-ttu-id="cbb51-180">Spécifie la valeur actuelle de la vitesse du vent numérique.</span><span class="sxs-lookup"><span data-stu-id="cbb51-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="cbb51-181">Valeur du type xs:integer</span><span class="sxs-lookup"><span data-stu-id="cbb51-181">A value of the type xs:integer</span></span>  <br/> |
   

