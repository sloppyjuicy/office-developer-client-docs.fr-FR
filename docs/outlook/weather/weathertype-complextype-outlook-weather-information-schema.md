---
title: complexType weatherType (Outlook Weather Information Schema)
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
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="e8962-103">complexType weatherType (Outlook Weather Information Schema)</span><span class="sxs-lookup"><span data-stu-id="e8962-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="e8962-104">Spécifie les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="e8962-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="e8962-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="e8962-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8962-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e8962-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="e8962-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e8962-107">**Schema file**</span></span> <br/> |<span data-ttu-id="e8962-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="e8962-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="e8962-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="e8962-109">**Extension base**</span></span> <br/> |<span data-ttu-id="e8962-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="e8962-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e8962-111">Définition</span><span class="sxs-lookup"><span data-stu-id="e8962-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e8962-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e8962-112">Elements and attributes</span></span>

<span data-ttu-id="e8962-113">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="e8962-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e8962-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e8962-114">Child elements</span></span>

|<span data-ttu-id="e8962-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e8962-115">**Element**</span></span>|<span data-ttu-id="e8962-116">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="e8962-116">**Type**</span></span>|<span data-ttu-id="e8962-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="e8962-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e8962-118">current</span><span class="sxs-lookup"><span data-stu-id="e8962-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="e8962-119">currentType</span><span class="sxs-lookup"><span data-stu-id="e8962-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="e8962-120">Spécifie les conditions météorologiques actuelles.</span><span class="sxs-lookup"><span data-stu-id="e8962-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="e8962-121">forecast</span><span class="sxs-lookup"><span data-stu-id="e8962-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="e8962-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="e8962-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="e8962-123">Spécifie les conditions météorologiques futures d’au moins trois jours à l’avance, y compris aujourd’hui : Aujourd’hui, Demain, Jour après Demain.</span><span class="sxs-lookup"><span data-stu-id="e8962-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e8962-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="e8962-124">Attributes</span></span>

|<span data-ttu-id="e8962-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e8962-125">**Attribute**</span></span>|<span data-ttu-id="e8962-126">**Type**</span><span class="sxs-lookup"><span data-stu-id="e8962-126">**Type**</span></span>|<span data-ttu-id="e8962-127">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e8962-127">**Required**</span></span>|<span data-ttu-id="e8962-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="e8962-128">**Description**</span></span>|<span data-ttu-id="e8962-129">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e8962-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e8962-130">attribution</span><span class="sxs-lookup"><span data-stu-id="e8962-130">attribution</span></span>  <br/> |<span data-ttu-id="e8962-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="e8962-131">xs:string</span></span>  <br/> |<span data-ttu-id="e8962-132">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e8962-132">required</span></span>  <br/> |<span data-ttu-id="e8962-133">Spécifie la source des informations météorologiques.</span><span class="sxs-lookup"><span data-stu-id="e8962-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="e8962-134">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="e8962-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="e8962-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="e8962-135">degreetype</span></span>  <br/> |<span data-ttu-id="e8962-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="e8962-136">xs:string</span></span>  <br/> |<span data-ttu-id="e8962-137">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e8962-137">required</span></span>  <br/> |<span data-ttu-id="e8962-138">Spécifie l’unité de température de l’emplacement, par exemple, Celsius.</span><span class="sxs-lookup"><span data-stu-id="e8962-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="e8962-139">C, F</span><span class="sxs-lookup"><span data-stu-id="e8962-139">C, F</span></span>  <br/> |
|<span data-ttu-id="e8962-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="e8962-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="e8962-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="e8962-141">xs:string</span></span>  <br/> |<span data-ttu-id="e8962-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e8962-142">required</span></span>  <br/> |<span data-ttu-id="e8962-143">Spécifie l’URL de l’image pour l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="e8962-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="e8962-144">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="e8962-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="e8962-145">timezone</span><span class="sxs-lookup"><span data-stu-id="e8962-145">timezone</span></span>  <br/> |<span data-ttu-id="e8962-146">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e8962-146">xs:integer</span></span>  <br/> |<span data-ttu-id="e8962-147">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e8962-147">required</span></span>  <br/> |<span data-ttu-id="e8962-148">Spécifie le décalage GMT.</span><span class="sxs-lookup"><span data-stu-id="e8962-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="e8962-149">Valeur entre -11 et 12 inclus</span><span class="sxs-lookup"><span data-stu-id="e8962-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="e8962-150">url</span><span class="sxs-lookup"><span data-stu-id="e8962-150">url</span></span>  <br/> |<span data-ttu-id="e8962-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="e8962-151">xs:string</span></span>  <br/> |<span data-ttu-id="e8962-152">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e8962-152">required</span></span>  <br/> |<span data-ttu-id="e8962-153">Spécifie l’URL de la page web du service météo qui contient des informations météorologiques pour l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8962-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="e8962-154">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="e8962-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="e8962-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="e8962-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="e8962-156">xs:string</span><span class="sxs-lookup"><span data-stu-id="e8962-156">xs:string</span></span>  <br/> |<span data-ttu-id="e8962-157">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e8962-157">required</span></span>  <br/> |<span data-ttu-id="e8962-158">Spécifie le code associé à l’emplacement utilisé pour distinguer plusieurs emplacements qui ont le même nom.</span><span class="sxs-lookup"><span data-stu-id="e8962-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="e8962-159">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="e8962-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="e8962-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="e8962-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="e8962-161">xs:string</span><span class="sxs-lookup"><span data-stu-id="e8962-161">xs:string</span></span>  <br/> |<span data-ttu-id="e8962-162">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e8962-162">required</span></span>  <br/> |<span data-ttu-id="e8962-163">Spécifie le nom de l’emplacement qui apparaît dans le contrôle de la zone de baisse.</span><span class="sxs-lookup"><span data-stu-id="e8962-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="e8962-164">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="e8962-164">A value of the type xs:string</span></span>  <br/> |
   

