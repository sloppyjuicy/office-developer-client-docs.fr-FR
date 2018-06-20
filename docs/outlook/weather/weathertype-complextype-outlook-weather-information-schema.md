---
title: type complexe weatherType (schéma des informations météo Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Spécifie les conditions météorologiques d’un emplacement.
ms.openlocfilehash: b333bb6ce60dd1613bceda0a57e7e34c9819bd84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787790"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="98ec4-103">type complexe weatherType (schéma des informations météo Outlook)</span><span class="sxs-lookup"><span data-stu-id="98ec4-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="98ec4-104">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="98ec4-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="98ec4-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="98ec4-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98ec4-106">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="98ec4-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="98ec4-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="98ec4-107">**Schema file**</span></span> <br/> |<span data-ttu-id="98ec4-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="98ec4-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="98ec4-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="98ec4-109">**Extension base**</span></span> <br/> |<span data-ttu-id="98ec4-110">Aucune</span><span class="sxs-lookup"><span data-stu-id="98ec4-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="98ec4-111">Définition</span><span class="sxs-lookup"><span data-stu-id="98ec4-111">Definition</span></span>

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="98ec4-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="98ec4-112">Elements and attributes</span></span>

<span data-ttu-id="98ec4-113">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="98ec4-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="98ec4-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="98ec4-114">Child elements</span></span>

|<span data-ttu-id="98ec4-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="98ec4-115">**Element**</span></span>|<span data-ttu-id="98ec4-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="98ec4-116">**Type**</span></span>|<span data-ttu-id="98ec4-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="98ec4-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="98ec4-118">en cours</span><span class="sxs-lookup"><span data-stu-id="98ec4-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="98ec4-119">currentType</span><span class="sxs-lookup"><span data-stu-id="98ec4-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="98ec4-120">Spécifie la météo.</span><span class="sxs-lookup"><span data-stu-id="98ec4-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="98ec4-121">prévision</span><span class="sxs-lookup"><span data-stu-id="98ec4-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="98ec4-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="98ec4-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="98ec4-123">Spécifie les conditions météo future d’au moins trois jours avance y compris aujourd'hui : aujourd'hui, demain, jour après demain.</span><span class="sxs-lookup"><span data-stu-id="98ec4-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="98ec4-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="98ec4-124">Attributes</span></span>

|<span data-ttu-id="98ec4-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="98ec4-125">**Attribute**</span></span>|<span data-ttu-id="98ec4-126">**Type**</span><span class="sxs-lookup"><span data-stu-id="98ec4-126">**Type**</span></span>|<span data-ttu-id="98ec4-127">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="98ec4-127">**Required**</span></span>|<span data-ttu-id="98ec4-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="98ec4-128">**Description**</span></span>|<span data-ttu-id="98ec4-129">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="98ec4-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="98ec4-130">attribution</span><span class="sxs-lookup"><span data-stu-id="98ec4-130">attribution</span></span>  <br/> |<span data-ttu-id="98ec4-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="98ec4-131">xs:string</span></span>  <br/> |<span data-ttu-id="98ec4-132">obligatoire</span><span class="sxs-lookup"><span data-stu-id="98ec4-132">required</span></span>  <br/> |<span data-ttu-id="98ec4-133">Spécifie la source de la météo.</span><span class="sxs-lookup"><span data-stu-id="98ec4-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="98ec4-134">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="98ec4-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="98ec4-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="98ec4-135">degreetype</span></span>  <br/> |<span data-ttu-id="98ec4-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="98ec4-136">xs:string</span></span>  <br/> |<span data-ttu-id="98ec4-137">obligatoire</span><span class="sxs-lookup"><span data-stu-id="98ec4-137">required</span></span>  <br/> |<span data-ttu-id="98ec4-138">Spécifie l’unité de la température de l’emplacement, par exemple, Celsius.</span><span class="sxs-lookup"><span data-stu-id="98ec4-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="98ec4-139">C, F</span><span class="sxs-lookup"><span data-stu-id="98ec4-139">C, F</span></span>  <br/> |
|<span data-ttu-id="98ec4-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="98ec4-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="98ec4-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="98ec4-141">xs:string</span></span>  <br/> |<span data-ttu-id="98ec4-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="98ec4-142">required</span></span>  <br/> |<span data-ttu-id="98ec4-143">Spécifie l’URL de l’image pour l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="98ec4-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="98ec4-144">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="98ec4-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="98ec4-145">fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="98ec4-145">timezone</span></span>  <br/> |<span data-ttu-id="98ec4-146">xs:integer</span><span class="sxs-lookup"><span data-stu-id="98ec4-146">xs:integer</span></span>  <br/> |<span data-ttu-id="98ec4-147">obligatoire</span><span class="sxs-lookup"><span data-stu-id="98ec4-147">required</span></span>  <br/> |<span data-ttu-id="98ec4-148">Spécifie le décalage GMT.</span><span class="sxs-lookup"><span data-stu-id="98ec4-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="98ec4-149">Une valeur comprise entre -11 et 12 inclus</span><span class="sxs-lookup"><span data-stu-id="98ec4-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="98ec4-150">url</span><span class="sxs-lookup"><span data-stu-id="98ec4-150">url</span></span>  <br/> |<span data-ttu-id="98ec4-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="98ec4-151">xs:string</span></span>  <br/> |<span data-ttu-id="98ec4-152">obligatoire</span><span class="sxs-lookup"><span data-stu-id="98ec4-152">required</span></span>  <br/> |<span data-ttu-id="98ec4-153">Spécifie l’URL de la page web du service météo qui contient des informations météorologiques pour l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="98ec4-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="98ec4-154">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="98ec4-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="98ec4-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="98ec4-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="98ec4-156">xs:string</span><span class="sxs-lookup"><span data-stu-id="98ec4-156">xs:string</span></span>  <br/> |<span data-ttu-id="98ec4-157">obligatoire</span><span class="sxs-lookup"><span data-stu-id="98ec4-157">required</span></span>  <br/> |<span data-ttu-id="98ec4-158">Spécifie le code qui est associé à l’emplacement permet de distinguer plusieurs emplacement ayant le même nom.</span><span class="sxs-lookup"><span data-stu-id="98ec4-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="98ec4-159">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="98ec4-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="98ec4-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="98ec4-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="98ec4-161">xs:string</span><span class="sxs-lookup"><span data-stu-id="98ec4-161">xs:string</span></span>  <br/> |<span data-ttu-id="98ec4-162">obligatoire</span><span class="sxs-lookup"><span data-stu-id="98ec4-162">required</span></span>  <br/> |<span data-ttu-id="98ec4-163">Spécifie le nom de l’emplacement qui s’affiche dans le contrôle de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="98ec4-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="98ec4-164">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="98ec4-164">A value of the type xs:string</span></span>  <br/> |
   

