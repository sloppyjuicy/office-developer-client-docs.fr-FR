---
title: complexType weatherType (schéma d'emplacement météorologique Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Définit les paramètres relatifs aux conditions météorologiques d'un emplacement.
ms.openlocfilehash: c3d640789cb68891878c3dca5210ab9dea280180
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355180"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="48c20-103">complexType weatherType (schéma d'emplacement météorologique Outlook)</span><span class="sxs-lookup"><span data-stu-id="48c20-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="48c20-104">Définit les paramètres relatifs aux conditions météorologiques d'un emplacement.</span><span class="sxs-lookup"><span data-stu-id="48c20-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="48c20-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="48c20-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48c20-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="48c20-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="48c20-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="48c20-107">**Schema file**</span></span> <br/> |<span data-ttu-id="48c20-108">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="48c20-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="48c20-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="48c20-109">**Extension base**</span></span> <br/> |<span data-ttu-id="48c20-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="48c20-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="48c20-111">Définition</span><span class="sxs-lookup"><span data-stu-id="48c20-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="48c20-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="48c20-112">Elements and attributes</span></span>

<span data-ttu-id="48c20-113">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="48c20-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="48c20-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="48c20-114">Child elements</span></span>

<span data-ttu-id="48c20-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="48c20-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48c20-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="48c20-116">Attributes</span></span>

|<span data-ttu-id="48c20-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="48c20-117">**Attribute**</span></span>|<span data-ttu-id="48c20-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="48c20-118">**Type**</span></span>|<span data-ttu-id="48c20-119">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="48c20-119">**Required**</span></span>|<span data-ttu-id="48c20-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="48c20-120">**Description**</span></span>|<span data-ttu-id="48c20-121">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="48c20-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="48c20-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="48c20-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="48c20-123">XS: String</span><span class="sxs-lookup"><span data-stu-id="48c20-123">xs:string</span></span>  <br/> |<span data-ttu-id="48c20-124">obligatoire</span><span class="sxs-lookup"><span data-stu-id="48c20-124">required</span></span>  <br/> |<span data-ttu-id="48c20-125">Spécifie un code associé à l'emplacement pour distinguer plusieurs emplacements portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="48c20-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="48c20-126">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="48c20-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="48c20-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="48c20-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="48c20-128">XS: String</span><span class="sxs-lookup"><span data-stu-id="48c20-128">xs:string</span></span>  <br/> |<span data-ttu-id="48c20-129">obligatoire</span><span class="sxs-lookup"><span data-stu-id="48c20-129">required</span></span>  <br/> |<span data-ttu-id="48c20-130">Spécifie le nom de l'emplacement.</span><span class="sxs-lookup"><span data-stu-id="48c20-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="48c20-131">Une valeur du type xs: String</span><span class="sxs-lookup"><span data-stu-id="48c20-131">A value of the type xs:string</span></span>  <br/> |
   

