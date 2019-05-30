---
title: complexType weatherType (schéma d’informations météorologiques Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Spécifie les conditions météorologiques d’un emplacement.
ms.openlocfilehash: ac7b8f37e71da203db0f6aefc8e20b29e810c3cf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542946"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="d43f5-103">complexType weatherType (schéma d’informations météorologiques Outlook)</span><span class="sxs-lookup"><span data-stu-id="d43f5-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="d43f5-104">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="d43f5-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="d43f5-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="d43f5-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d43f5-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d43f5-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="d43f5-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d43f5-107">**Schema file**</span></span> <br/> |<span data-ttu-id="d43f5-108">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="d43f5-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="d43f5-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="d43f5-109">**Extension base**</span></span> <br/> |<span data-ttu-id="d43f5-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="d43f5-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d43f5-111">Définition</span><span class="sxs-lookup"><span data-stu-id="d43f5-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d43f5-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d43f5-112">Elements and attributes</span></span>

<span data-ttu-id="d43f5-113">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="d43f5-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d43f5-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d43f5-114">Child elements</span></span>

|<span data-ttu-id="d43f5-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d43f5-115">**Element**</span></span>|<span data-ttu-id="d43f5-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="d43f5-116">**Type**</span></span>|<span data-ttu-id="d43f5-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="d43f5-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d43f5-118">récent</span><span class="sxs-lookup"><span data-stu-id="d43f5-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="d43f5-119">currentType</span><span class="sxs-lookup"><span data-stu-id="d43f5-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="d43f5-120">Spécifie les conditions météorologiques actuelles.</span><span class="sxs-lookup"><span data-stu-id="d43f5-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="d43f5-121">prévisionnel</span><span class="sxs-lookup"><span data-stu-id="d43f5-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="d43f5-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="d43f5-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="d43f5-123">Spécifie les conditions météorologiques futures d’une avance de trois jours, y compris aujourd’hui: aujourd’hui, demain, jour après demain.</span><span class="sxs-lookup"><span data-stu-id="d43f5-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d43f5-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="d43f5-124">Attributes</span></span>

|<span data-ttu-id="d43f5-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d43f5-125">**Attribute**</span></span>|<span data-ttu-id="d43f5-126">**Type**</span><span class="sxs-lookup"><span data-stu-id="d43f5-126">**Type**</span></span>|<span data-ttu-id="d43f5-127">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d43f5-127">**Required**</span></span>|<span data-ttu-id="d43f5-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="d43f5-128">**Description**</span></span>|<span data-ttu-id="d43f5-129">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="d43f5-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d43f5-130">attribution</span><span class="sxs-lookup"><span data-stu-id="d43f5-130">attribution</span></span>  <br/> |<span data-ttu-id="d43f5-131">XS: String</span><span class="sxs-lookup"><span data-stu-id="d43f5-131">xs:string</span></span>  <br/> |<span data-ttu-id="d43f5-132">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d43f5-132">required</span></span>  <br/> |<span data-ttu-id="d43f5-133">Spécifie la source des informations météorologiques.</span><span class="sxs-lookup"><span data-stu-id="d43f5-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="d43f5-134">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="d43f5-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d43f5-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="d43f5-135">degreetype</span></span>  <br/> |<span data-ttu-id="d43f5-136">XS: String</span><span class="sxs-lookup"><span data-stu-id="d43f5-136">xs:string</span></span>  <br/> |<span data-ttu-id="d43f5-137">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d43f5-137">required</span></span>  <br/> |<span data-ttu-id="d43f5-138">Indique l’unité de température de l’emplacement (par exemple, Celsius).</span><span class="sxs-lookup"><span data-stu-id="d43f5-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="d43f5-139">C, F</span><span class="sxs-lookup"><span data-stu-id="d43f5-139">C, F</span></span>  <br/> |
|<span data-ttu-id="d43f5-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="d43f5-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="d43f5-141">XS: String</span><span class="sxs-lookup"><span data-stu-id="d43f5-141">xs:string</span></span>  <br/> |<span data-ttu-id="d43f5-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d43f5-142">required</span></span>  <br/> |<span data-ttu-id="d43f5-143">Spécifie l’URL de l’image pour l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="d43f5-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="d43f5-144">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="d43f5-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d43f5-145">horaire</span><span class="sxs-lookup"><span data-stu-id="d43f5-145">timezone</span></span>  <br/> |<span data-ttu-id="d43f5-146">XS: Integer</span><span class="sxs-lookup"><span data-stu-id="d43f5-146">xs:integer</span></span>  <br/> |<span data-ttu-id="d43f5-147">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d43f5-147">required</span></span>  <br/> |<span data-ttu-id="d43f5-148">Spécifie le décalage GMT.</span><span class="sxs-lookup"><span data-stu-id="d43f5-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="d43f5-149">Une valeur comprise entre-11 et 12 inclus</span><span class="sxs-lookup"><span data-stu-id="d43f5-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="d43f5-150">url</span><span class="sxs-lookup"><span data-stu-id="d43f5-150">url</span></span>  <br/> |<span data-ttu-id="d43f5-151">XS: String</span><span class="sxs-lookup"><span data-stu-id="d43f5-151">xs:string</span></span>  <br/> |<span data-ttu-id="d43f5-152">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d43f5-152">required</span></span>  <br/> |<span data-ttu-id="d43f5-153">Spécifie l’URL de la page Web du service météo qui contient des informations météorologiques pour l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="d43f5-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="d43f5-154">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="d43f5-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d43f5-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="d43f5-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="d43f5-156">XS: String</span><span class="sxs-lookup"><span data-stu-id="d43f5-156">xs:string</span></span>  <br/> |<span data-ttu-id="d43f5-157">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d43f5-157">required</span></span>  <br/> |<span data-ttu-id="d43f5-158">Spécifie le code associé à l’emplacement utilisé pour distinguer plusieurs emplacements portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="d43f5-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="d43f5-159">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="d43f5-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d43f5-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="d43f5-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="d43f5-161">XS: String</span><span class="sxs-lookup"><span data-stu-id="d43f5-161">xs:string</span></span>  <br/> |<span data-ttu-id="d43f5-162">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d43f5-162">required</span></span>  <br/> |<span data-ttu-id="d43f5-163">Spécifie le nom de l’emplacement qui apparaît dans le contrôle de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d43f5-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="d43f5-164">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="d43f5-164">A value of the type xs:string</span></span>  <br/> |
   

