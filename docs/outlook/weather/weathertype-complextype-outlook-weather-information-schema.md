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
ms.openlocfilehash: ffa91c4982b5703041c79b47eb15a3a2b845b429
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398765"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="c4ece-103">type complexe weatherType (schéma des informations météo Outlook)</span><span class="sxs-lookup"><span data-stu-id="c4ece-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="c4ece-104">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="c4ece-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="c4ece-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c4ece-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4ece-106">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c4ece-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="c4ece-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c4ece-107">**Schema file**</span></span> <br/> |<span data-ttu-id="c4ece-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="c4ece-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="c4ece-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c4ece-109">**Extension base**</span></span> <br/> |<span data-ttu-id="c4ece-110">Aucune</span><span class="sxs-lookup"><span data-stu-id="c4ece-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c4ece-111">Définition</span><span class="sxs-lookup"><span data-stu-id="c4ece-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c4ece-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c4ece-112">Elements and attributes</span></span>

<span data-ttu-id="c4ece-113">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c4ece-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c4ece-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c4ece-114">Child elements</span></span>

|<span data-ttu-id="c4ece-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c4ece-115">**Element**</span></span>|<span data-ttu-id="c4ece-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="c4ece-116">**Type**</span></span>|<span data-ttu-id="c4ece-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="c4ece-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c4ece-118">en cours</span><span class="sxs-lookup"><span data-stu-id="c4ece-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="c4ece-119">currentType</span><span class="sxs-lookup"><span data-stu-id="c4ece-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="c4ece-120">Spécifie la météo.</span><span class="sxs-lookup"><span data-stu-id="c4ece-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="c4ece-121">prévision</span><span class="sxs-lookup"><span data-stu-id="c4ece-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="c4ece-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="c4ece-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="c4ece-123">Spécifie les conditions météo future d’au moins trois jours avance y compris aujourd'hui : aujourd'hui, demain, jour après demain.</span><span class="sxs-lookup"><span data-stu-id="c4ece-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c4ece-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="c4ece-124">Attributes</span></span>

|<span data-ttu-id="c4ece-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c4ece-125">**Attribute**</span></span>|<span data-ttu-id="c4ece-126">**Type**</span><span class="sxs-lookup"><span data-stu-id="c4ece-126">**Type**</span></span>|<span data-ttu-id="c4ece-127">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c4ece-127">**Required**</span></span>|<span data-ttu-id="c4ece-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="c4ece-128">**Description**</span></span>|<span data-ttu-id="c4ece-129">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c4ece-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c4ece-130">attribution</span><span class="sxs-lookup"><span data-stu-id="c4ece-130">attribution</span></span>  <br/> |<span data-ttu-id="c4ece-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="c4ece-131">xs:string</span></span>  <br/> |<span data-ttu-id="c4ece-132">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4ece-132">required</span></span>  <br/> |<span data-ttu-id="c4ece-133">Spécifie la source de la météo.</span><span class="sxs-lookup"><span data-stu-id="c4ece-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="c4ece-134">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="c4ece-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="c4ece-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="c4ece-135">degreetype</span></span>  <br/> |<span data-ttu-id="c4ece-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="c4ece-136">xs:string</span></span>  <br/> |<span data-ttu-id="c4ece-137">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4ece-137">required</span></span>  <br/> |<span data-ttu-id="c4ece-138">Spécifie l’unité de la température de l’emplacement, par exemple, Celsius.</span><span class="sxs-lookup"><span data-stu-id="c4ece-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="c4ece-139">C, F</span><span class="sxs-lookup"><span data-stu-id="c4ece-139">C, F</span></span>  <br/> |
|<span data-ttu-id="c4ece-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="c4ece-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="c4ece-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="c4ece-141">xs:string</span></span>  <br/> |<span data-ttu-id="c4ece-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4ece-142">required</span></span>  <br/> |<span data-ttu-id="c4ece-143">Spécifie l’URL de l’image pour l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="c4ece-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="c4ece-144">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="c4ece-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="c4ece-145">fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="c4ece-145">timezone</span></span>  <br/> |<span data-ttu-id="c4ece-146">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c4ece-146">xs:integer</span></span>  <br/> |<span data-ttu-id="c4ece-147">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4ece-147">required</span></span>  <br/> |<span data-ttu-id="c4ece-148">Spécifie le décalage GMT.</span><span class="sxs-lookup"><span data-stu-id="c4ece-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="c4ece-149">Une valeur comprise entre -11 et 12 inclus</span><span class="sxs-lookup"><span data-stu-id="c4ece-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="c4ece-150">url</span><span class="sxs-lookup"><span data-stu-id="c4ece-150">url</span></span>  <br/> |<span data-ttu-id="c4ece-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="c4ece-151">xs:string</span></span>  <br/> |<span data-ttu-id="c4ece-152">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4ece-152">required</span></span>  <br/> |<span data-ttu-id="c4ece-153">Spécifie l’URL de la page web du service météo qui contient des informations météorologiques pour l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="c4ece-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="c4ece-154">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="c4ece-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="c4ece-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="c4ece-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="c4ece-156">xs:string</span><span class="sxs-lookup"><span data-stu-id="c4ece-156">xs:string</span></span>  <br/> |<span data-ttu-id="c4ece-157">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4ece-157">required</span></span>  <br/> |<span data-ttu-id="c4ece-158">Spécifie le code qui est associé à l’emplacement permet de distinguer plusieurs emplacement ayant le même nom.</span><span class="sxs-lookup"><span data-stu-id="c4ece-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="c4ece-159">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="c4ece-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="c4ece-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="c4ece-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="c4ece-161">xs:string</span><span class="sxs-lookup"><span data-stu-id="c4ece-161">xs:string</span></span>  <br/> |<span data-ttu-id="c4ece-162">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c4ece-162">required</span></span>  <br/> |<span data-ttu-id="c4ece-163">Spécifie le nom de l’emplacement qui s’affiche dans le contrôle de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c4ece-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="c4ece-164">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="c4ece-164">A value of the type xs:string</span></span>  <br/> |
   

