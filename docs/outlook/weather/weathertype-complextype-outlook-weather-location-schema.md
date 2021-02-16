---
title: complexType weatherType (outlook weather location schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Définit les paramètres sur les conditions météorologiques d’un emplacement.
ms.openlocfilehash: f7d33cb018daf4ece2ba468b9ebe92b0fc7b1545
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542918"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="63735-103">complexType weatherType (outlook weather location schema)</span><span class="sxs-lookup"><span data-stu-id="63735-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="63735-104">Définit les paramètres sur les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="63735-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="63735-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="63735-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63735-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="63735-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="63735-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="63735-107">**Schema file**</span></span> <br/> |<span data-ttu-id="63735-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="63735-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="63735-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="63735-109">**Extension base**</span></span> <br/> |<span data-ttu-id="63735-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="63735-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="63735-111">Définition</span><span class="sxs-lookup"><span data-stu-id="63735-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="63735-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="63735-112">Elements and attributes</span></span>

<span data-ttu-id="63735-113">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="63735-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="63735-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="63735-114">Child elements</span></span>

<span data-ttu-id="63735-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="63735-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63735-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="63735-116">Attributes</span></span>

|<span data-ttu-id="63735-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="63735-117">**Attribute**</span></span>|<span data-ttu-id="63735-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="63735-118">**Type**</span></span>|<span data-ttu-id="63735-119">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="63735-119">**Required**</span></span>|<span data-ttu-id="63735-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="63735-120">**Description**</span></span>|<span data-ttu-id="63735-121">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="63735-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="63735-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="63735-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="63735-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="63735-123">xs:string</span></span>  <br/> |<span data-ttu-id="63735-124">obligatoire</span><span class="sxs-lookup"><span data-stu-id="63735-124">required</span></span>  <br/> |<span data-ttu-id="63735-125">Spécifie un code associé à l’emplacement pour distinguer plusieurs emplacements du même nom.</span><span class="sxs-lookup"><span data-stu-id="63735-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="63735-126">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="63735-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="63735-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="63735-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="63735-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="63735-128">xs:string</span></span>  <br/> |<span data-ttu-id="63735-129">obligatoire</span><span class="sxs-lookup"><span data-stu-id="63735-129">required</span></span>  <br/> |<span data-ttu-id="63735-130">Spécifie le nom de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="63735-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="63735-131">Valeur du type xs:string</span><span class="sxs-lookup"><span data-stu-id="63735-131">A value of the type xs:string</span></span>  <br/> |
   

