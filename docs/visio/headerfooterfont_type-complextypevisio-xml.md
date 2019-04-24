---
title: ComplexType HeaderFooterFont_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335622"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="857ec-102">ComplexType HeaderFooterFont_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="857ec-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="857ec-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="857ec-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="857ec-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="857ec-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="857ec-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="857ec-105">**Schema file**</span></span> <br/> |<span data-ttu-id="857ec-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="857ec-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="857ec-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="857ec-107">**Extension base**</span></span> <br/> |<span data-ttu-id="857ec-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="857ec-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="857ec-109">Définition</span><span class="sxs-lookup"><span data-stu-id="857ec-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="857ec-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="857ec-110">Elements and attributes</span></span>

<span data-ttu-id="857ec-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="857ec-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="857ec-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="857ec-112">Child elements</span></span>

<span data-ttu-id="857ec-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="857ec-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="857ec-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="857ec-114">Attributes</span></span>

|<span data-ttu-id="857ec-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="857ec-115">**Attribute**</span></span>|<span data-ttu-id="857ec-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="857ec-116">**Type**</span></span>|<span data-ttu-id="857ec-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="857ec-117">**Required**</span></span>|<span data-ttu-id="857ec-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="857ec-118">**Description**</span></span>|<span data-ttu-id="857ec-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="857ec-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="857ec-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="857ec-120">CharSet</span></span>  <br/> |<span data-ttu-id="857ec-121">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="857ec-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="857ec-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-122">optional</span></span>  <br/> ||<span data-ttu-id="857ec-123">Valeurs du type xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="857ec-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="857ec-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="857ec-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="857ec-125">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="857ec-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="857ec-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-126">optional</span></span>  <br/> ||<span data-ttu-id="857ec-127">Valeurs du type xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="857ec-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="857ec-128">Échappement</span><span class="sxs-lookup"><span data-stu-id="857ec-128">Escapement</span></span>  <br/> |<span data-ttu-id="857ec-129">xsd: int</span><span class="sxs-lookup"><span data-stu-id="857ec-129">xsd:int</span></span>  <br/> |<span data-ttu-id="857ec-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-130">optional</span></span>  <br/> ||<span data-ttu-id="857ec-131">Valeurs du type xsd: int.</span><span class="sxs-lookup"><span data-stu-id="857ec-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="857ec-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="857ec-132">FaceName</span></span>  <br/> |<span data-ttu-id="857ec-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="857ec-133">xsd:string</span></span>  <br/> |<span data-ttu-id="857ec-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-134">optional</span></span>  <br/> ||<span data-ttu-id="857ec-135">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="857ec-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="857ec-136">Hauteur</span><span class="sxs-lookup"><span data-stu-id="857ec-136">Height</span></span>  <br/> |<span data-ttu-id="857ec-137">xsd: int</span><span class="sxs-lookup"><span data-stu-id="857ec-137">xsd:int</span></span>  <br/> |<span data-ttu-id="857ec-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-138">optional</span></span>  <br/> ||<span data-ttu-id="857ec-139">Valeurs du type xsd: int.</span><span class="sxs-lookup"><span data-stu-id="857ec-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="857ec-140">Italic</span><span class="sxs-lookup"><span data-stu-id="857ec-140">Italic</span></span>  <br/> |<span data-ttu-id="857ec-141">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="857ec-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="857ec-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-142">optional</span></span>  <br/> ||<span data-ttu-id="857ec-143">Valeurs du type xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="857ec-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="857ec-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="857ec-144">Orientation</span></span>  <br/> |<span data-ttu-id="857ec-145">xsd: int</span><span class="sxs-lookup"><span data-stu-id="857ec-145">xsd:int</span></span>  <br/> |<span data-ttu-id="857ec-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-146">optional</span></span>  <br/> ||<span data-ttu-id="857ec-147">Valeurs du type xsd: int.</span><span class="sxs-lookup"><span data-stu-id="857ec-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="857ec-148">La précision</span><span class="sxs-lookup"><span data-stu-id="857ec-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="857ec-149">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="857ec-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="857ec-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-150">optional</span></span>  <br/> ||<span data-ttu-id="857ec-151">Valeurs du type xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="857ec-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="857ec-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="857ec-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="857ec-153">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="857ec-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="857ec-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-154">optional</span></span>  <br/> ||<span data-ttu-id="857ec-155">Valeurs du type xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="857ec-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="857ec-156">Quality</span><span class="sxs-lookup"><span data-stu-id="857ec-156">Quality</span></span>  <br/> |<span data-ttu-id="857ec-157">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="857ec-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="857ec-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-158">optional</span></span>  <br/> ||<span data-ttu-id="857ec-159">Valeurs du type xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="857ec-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="857ec-160">Barré</span><span class="sxs-lookup"><span data-stu-id="857ec-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="857ec-161">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="857ec-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="857ec-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-162">optional</span></span>  <br/> ||<span data-ttu-id="857ec-163">Valeurs du type xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="857ec-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="857ec-164">Underline</span><span class="sxs-lookup"><span data-stu-id="857ec-164">Underline</span></span>  <br/> |<span data-ttu-id="857ec-165">xsd: unsignedByte</span><span class="sxs-lookup"><span data-stu-id="857ec-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="857ec-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-166">optional</span></span>  <br/> ||<span data-ttu-id="857ec-167">Valeurs du type xsd: unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="857ec-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="857ec-168">Pondération</span><span class="sxs-lookup"><span data-stu-id="857ec-168">Weight</span></span>  <br/> |<span data-ttu-id="857ec-169">xsd: int</span><span class="sxs-lookup"><span data-stu-id="857ec-169">xsd:int</span></span>  <br/> |<span data-ttu-id="857ec-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-170">optional</span></span>  <br/> ||<span data-ttu-id="857ec-171">Valeurs du type xsd: int.</span><span class="sxs-lookup"><span data-stu-id="857ec-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="857ec-172">Largeur</span><span class="sxs-lookup"><span data-stu-id="857ec-172">Width</span></span>  <br/> |<span data-ttu-id="857ec-173">xsd: int</span><span class="sxs-lookup"><span data-stu-id="857ec-173">xsd:int</span></span>  <br/> |<span data-ttu-id="857ec-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="857ec-174">optional</span></span>  <br/> ||<span data-ttu-id="857ec-175">Valeurs du type xsd: int.</span><span class="sxs-lookup"><span data-stu-id="857ec-175">Values of the xsd:int type.</span></span>  <br/> |
   

