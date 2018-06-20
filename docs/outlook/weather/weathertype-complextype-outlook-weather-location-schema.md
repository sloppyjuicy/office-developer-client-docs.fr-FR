---
title: type complexe weatherType (Outlook météo emplacement schéma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Définit les paramètres sur les conditions météorologiques d’un emplacement.
ms.openlocfilehash: 39dcc63dfc9b7a97b9643e804329fd1795d39201
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787804"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="a2325-103">type complexe weatherType (Outlook météo emplacement schéma)</span><span class="sxs-lookup"><span data-stu-id="a2325-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="a2325-104">Définit les paramètres sur les conditions météorologiques d’un emplacement.</span><span class="sxs-lookup"><span data-stu-id="a2325-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="a2325-105">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a2325-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2325-106">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="a2325-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="a2325-107">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a2325-107">**Schema file**</span></span> <br/> |<span data-ttu-id="a2325-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="a2325-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="a2325-109">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a2325-109">**Extension base**</span></span> <br/> |<span data-ttu-id="a2325-110">Aucune</span><span class="sxs-lookup"><span data-stu-id="a2325-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a2325-111">Définition</span><span class="sxs-lookup"><span data-stu-id="a2325-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="a2325-112">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a2325-112">Elements and attributes</span></span>

<span data-ttu-id="a2325-113">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="a2325-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a2325-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a2325-114">Child elements</span></span>

<span data-ttu-id="a2325-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a2325-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2325-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="a2325-116">Attributes</span></span>

|<span data-ttu-id="a2325-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a2325-117">**Attribute**</span></span>|<span data-ttu-id="a2325-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="a2325-118">**Type**</span></span>|<span data-ttu-id="a2325-119">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a2325-119">**Required**</span></span>|<span data-ttu-id="a2325-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="a2325-120">**Description**</span></span>|<span data-ttu-id="a2325-121">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a2325-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a2325-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="a2325-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="a2325-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2325-123">xs:string</span></span>  <br/> |<span data-ttu-id="a2325-124">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a2325-124">required</span></span>  <br/> |<span data-ttu-id="a2325-125">Spécifie un code qui est associé à l’emplacement pour distinguer plusieurs emplacements portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="a2325-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="a2325-126">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="a2325-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a2325-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="a2325-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="a2325-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="a2325-128">xs:string</span></span>  <br/> |<span data-ttu-id="a2325-129">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a2325-129">required</span></span>  <br/> |<span data-ttu-id="a2325-130">Spécifie le nom de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="a2325-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="a2325-131">Valeur du type xs : String</span><span class="sxs-lookup"><span data-stu-id="a2325-131">A value of the type xs:string</span></span>  <br/> |
   

