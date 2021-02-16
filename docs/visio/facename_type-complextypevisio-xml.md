---
title: FaceName_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: f0a136cec6d620ba7001ed0e6fae01af82c2180d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542897"
---
# <a name="facename_type-complextype-visio-xml"></a><span data-ttu-id="79dbf-102">FaceName_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="79dbf-102">FaceName_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="79dbf-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="79dbf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79dbf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="79dbf-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="79dbf-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="79dbf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="79dbf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="79dbf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="79dbf-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="79dbf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="79dbf-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="79dbf-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="79dbf-109">Définition</span><span class="sxs-lookup"><span data-stu-id="79dbf-109">Definition</span></span>

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="79dbf-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="79dbf-110">Elements and attributes</span></span>

<span data-ttu-id="79dbf-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="79dbf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="79dbf-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="79dbf-112">Child elements</span></span>

<span data-ttu-id="79dbf-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="79dbf-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="79dbf-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="79dbf-114">Attributes</span></span>

|<span data-ttu-id="79dbf-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="79dbf-115">**Attribute**</span></span>|<span data-ttu-id="79dbf-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="79dbf-116">**Type**</span></span>|<span data-ttu-id="79dbf-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="79dbf-117">**Required**</span></span>|<span data-ttu-id="79dbf-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="79dbf-118">**Description**</span></span>|<span data-ttu-id="79dbf-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="79dbf-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="79dbf-120">CharSets</span><span class="sxs-lookup"><span data-stu-id="79dbf-120">CharSets</span></span>  <br/> |<span data-ttu-id="79dbf-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="79dbf-121">xsd:string</span></span>  <br/> |<span data-ttu-id="79dbf-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="79dbf-122">optional</span></span>  <br/> ||<span data-ttu-id="79dbf-123">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="79dbf-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="79dbf-124">Flags</span><span class="sxs-lookup"><span data-stu-id="79dbf-124">Flags</span></span>  <br/> |<span data-ttu-id="79dbf-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="79dbf-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="79dbf-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="79dbf-126">optional</span></span>  <br/> ||<span data-ttu-id="79dbf-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="79dbf-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="79dbf-128">NameU</span><span class="sxs-lookup"><span data-stu-id="79dbf-128">NameU</span></span>  <br/> |<span data-ttu-id="79dbf-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="79dbf-129">xsd:string</span></span>  <br/> |<span data-ttu-id="79dbf-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="79dbf-130">required</span></span>  <br/> ||<span data-ttu-id="79dbf-131">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="79dbf-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="79dbf-132">Panos</span><span class="sxs-lookup"><span data-stu-id="79dbf-132">Panos</span></span>  <br/> |<span data-ttu-id="79dbf-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="79dbf-133">xsd:string</span></span>  <br/> |<span data-ttu-id="79dbf-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="79dbf-134">optional</span></span>  <br/> ||<span data-ttu-id="79dbf-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="79dbf-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="79dbf-136">Volet</span><span class="sxs-lookup"><span data-stu-id="79dbf-136">Panose</span></span>  <br/> |<span data-ttu-id="79dbf-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="79dbf-137">xsd:string</span></span>  <br/> |<span data-ttu-id="79dbf-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="79dbf-138">optional</span></span>  <br/> ||<span data-ttu-id="79dbf-139">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="79dbf-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="79dbf-140">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="79dbf-140">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="79dbf-141">xsd:string</span><span class="sxs-lookup"><span data-stu-id="79dbf-141">xsd:string</span></span>  <br/> |<span data-ttu-id="79dbf-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="79dbf-142">optional</span></span>  <br/> ||<span data-ttu-id="79dbf-143">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="79dbf-143">Values of the xsd:string type.</span></span>  <br/> |
   

