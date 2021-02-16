---
title: weather element (weatherdata element) (Outlook Weather Location Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Spécifie l’emplacement où signaler la météo.
ms.openlocfilehash: a907fb9df02d88d317a73e409ea8738273eb2cb1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539011"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="ff93f-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span><span class="sxs-lookup"><span data-stu-id="ff93f-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="ff93f-104">Spécifie l’emplacement où signaler la météo.</span><span class="sxs-lookup"><span data-stu-id="ff93f-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff93f-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="ff93f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff93f-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ff93f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ff93f-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="ff93f-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="ff93f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ff93f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="ff93f-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ff93f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ff93f-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="ff93f-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ff93f-111">Définition</span><span class="sxs-lookup"><span data-stu-id="ff93f-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="ff93f-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ff93f-112">Elements and attributes</span></span>

<span data-ttu-id="ff93f-113">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="ff93f-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ff93f-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ff93f-114">Parent elements</span></span>

|<span data-ttu-id="ff93f-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ff93f-115">**Element**</span></span>|<span data-ttu-id="ff93f-116">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="ff93f-116">**Type**</span></span>|<span data-ttu-id="ff93f-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="ff93f-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ff93f-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="ff93f-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="ff93f-119">Définit l’élément météo.</span><span class="sxs-lookup"><span data-stu-id="ff93f-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ff93f-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ff93f-120">Child elements</span></span>

<span data-ttu-id="ff93f-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ff93f-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff93f-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="ff93f-122">Attributes</span></span>

|<span data-ttu-id="ff93f-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ff93f-123">**Attribute**</span></span>|<span data-ttu-id="ff93f-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="ff93f-124">**Type**</span></span>|<span data-ttu-id="ff93f-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ff93f-125">**Required**</span></span>|<span data-ttu-id="ff93f-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="ff93f-126">**Description**</span></span>|<span data-ttu-id="ff93f-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ff93f-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ff93f-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="ff93f-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="ff93f-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="ff93f-129">xs:string</span></span>  <br/> |<span data-ttu-id="ff93f-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ff93f-130">required</span></span>  <br/> |<span data-ttu-id="ff93f-131">Spécifie un code associé à l’emplacement pour distinguer plusieurs emplacements du même nom.</span><span class="sxs-lookup"><span data-stu-id="ff93f-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="ff93f-132">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="ff93f-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="ff93f-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="ff93f-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="ff93f-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="ff93f-134">xs:string</span></span>  <br/> |<span data-ttu-id="ff93f-135">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ff93f-135">required</span></span>  <br/> |<span data-ttu-id="ff93f-136">Spécifie le nom de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="ff93f-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="ff93f-137">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="ff93f-137">A value of the type xs:string</span></span>  <br/> |
   

