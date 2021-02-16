---
title: HeaderFooterFont_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: dd99d87e0d80aad3bcde31e4834337ee59088da2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541070"
---
# <a name="headerfooterfont_type-complextype-visio-xml"></a><span data-ttu-id="28b33-102">HeaderFooterFont_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="28b33-102">HeaderFooterFont_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="28b33-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="28b33-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28b33-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="28b33-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="28b33-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="28b33-105">**Schema file**</span></span> <br/> |<span data-ttu-id="28b33-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="28b33-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="28b33-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="28b33-107">**Extension base**</span></span> <br/> |<span data-ttu-id="28b33-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="28b33-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="28b33-109">Définition</span><span class="sxs-lookup"><span data-stu-id="28b33-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="28b33-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="28b33-110">Elements and attributes</span></span>

<span data-ttu-id="28b33-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="28b33-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="28b33-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="28b33-112">Child elements</span></span>

<span data-ttu-id="28b33-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="28b33-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28b33-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="28b33-114">Attributes</span></span>

|<span data-ttu-id="28b33-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="28b33-115">**Attribute**</span></span>|<span data-ttu-id="28b33-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="28b33-116">**Type**</span></span>|<span data-ttu-id="28b33-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="28b33-117">**Required**</span></span>|<span data-ttu-id="28b33-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="28b33-118">**Description**</span></span>|<span data-ttu-id="28b33-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="28b33-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="28b33-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="28b33-120">CharSet</span></span>  <br/> |<span data-ttu-id="28b33-121">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="28b33-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="28b33-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-122">optional</span></span>  <br/> ||<span data-ttu-id="28b33-123">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="28b33-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="28b33-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="28b33-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="28b33-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="28b33-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="28b33-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-126">optional</span></span>  <br/> ||<span data-ttu-id="28b33-127">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="28b33-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="28b33-128">Escapement</span><span class="sxs-lookup"><span data-stu-id="28b33-128">Escapement</span></span>  <br/> |<span data-ttu-id="28b33-129">xsd:int</span><span class="sxs-lookup"><span data-stu-id="28b33-129">xsd:int</span></span>  <br/> |<span data-ttu-id="28b33-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-130">optional</span></span>  <br/> ||<span data-ttu-id="28b33-131">Valeurs du type xsd:int.</span><span class="sxs-lookup"><span data-stu-id="28b33-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="28b33-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="28b33-132">FaceName</span></span>  <br/> |<span data-ttu-id="28b33-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="28b33-133">xsd:string</span></span>  <br/> |<span data-ttu-id="28b33-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-134">optional</span></span>  <br/> ||<span data-ttu-id="28b33-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="28b33-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="28b33-136">Hauteur</span><span class="sxs-lookup"><span data-stu-id="28b33-136">Height</span></span>  <br/> |<span data-ttu-id="28b33-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="28b33-137">xsd:int</span></span>  <br/> |<span data-ttu-id="28b33-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-138">optional</span></span>  <br/> ||<span data-ttu-id="28b33-139">Valeurs du type xsd:int.</span><span class="sxs-lookup"><span data-stu-id="28b33-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="28b33-140">Italic</span><span class="sxs-lookup"><span data-stu-id="28b33-140">Italic</span></span>  <br/> |<span data-ttu-id="28b33-141">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="28b33-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="28b33-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-142">optional</span></span>  <br/> ||<span data-ttu-id="28b33-143">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="28b33-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="28b33-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="28b33-144">Orientation</span></span>  <br/> |<span data-ttu-id="28b33-145">xsd:int</span><span class="sxs-lookup"><span data-stu-id="28b33-145">xsd:int</span></span>  <br/> |<span data-ttu-id="28b33-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-146">optional</span></span>  <br/> ||<span data-ttu-id="28b33-147">Valeurs du type xsd:int.</span><span class="sxs-lookup"><span data-stu-id="28b33-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="28b33-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="28b33-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="28b33-149">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="28b33-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="28b33-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-150">optional</span></span>  <br/> ||<span data-ttu-id="28b33-151">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="28b33-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="28b33-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="28b33-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="28b33-153">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="28b33-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="28b33-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-154">optional</span></span>  <br/> ||<span data-ttu-id="28b33-155">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="28b33-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="28b33-156">Qualité</span><span class="sxs-lookup"><span data-stu-id="28b33-156">Quality</span></span>  <br/> |<span data-ttu-id="28b33-157">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="28b33-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="28b33-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-158">optional</span></span>  <br/> ||<span data-ttu-id="28b33-159">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="28b33-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="28b33-160">StrikeOut</span><span class="sxs-lookup"><span data-stu-id="28b33-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="28b33-161">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="28b33-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="28b33-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-162">optional</span></span>  <br/> ||<span data-ttu-id="28b33-163">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="28b33-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="28b33-164">Souligner</span><span class="sxs-lookup"><span data-stu-id="28b33-164">Underline</span></span>  <br/> |<span data-ttu-id="28b33-165">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="28b33-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="28b33-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-166">optional</span></span>  <br/> ||<span data-ttu-id="28b33-167">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="28b33-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="28b33-168">Pondération</span><span class="sxs-lookup"><span data-stu-id="28b33-168">Weight</span></span>  <br/> |<span data-ttu-id="28b33-169">xsd:int</span><span class="sxs-lookup"><span data-stu-id="28b33-169">xsd:int</span></span>  <br/> |<span data-ttu-id="28b33-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-170">optional</span></span>  <br/> ||<span data-ttu-id="28b33-171">Valeurs du type xsd:int.</span><span class="sxs-lookup"><span data-stu-id="28b33-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="28b33-172">Largeur</span><span class="sxs-lookup"><span data-stu-id="28b33-172">Width</span></span>  <br/> |<span data-ttu-id="28b33-173">xsd:int</span><span class="sxs-lookup"><span data-stu-id="28b33-173">xsd:int</span></span>  <br/> |<span data-ttu-id="28b33-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="28b33-174">optional</span></span>  <br/> ||<span data-ttu-id="28b33-175">Valeurs du type xsd:int.</span><span class="sxs-lookup"><span data-stu-id="28b33-175">Values of the xsd:int type.</span></span>  <br/> |
   

