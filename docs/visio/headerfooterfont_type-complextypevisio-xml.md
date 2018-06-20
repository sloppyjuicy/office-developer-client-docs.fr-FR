---
title: Type complexe HeaderFooterFont_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: 1d7c4d6850e4a8ea1933ae751c580d09e0dd67bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788754"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="47182-102">Type complexe HeaderFooterFont_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="47182-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="47182-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="47182-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47182-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="47182-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="47182-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="47182-105">**Schema file**</span></span> <br/> |<span data-ttu-id="47182-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="47182-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="47182-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="47182-107">**Extension base**</span></span> <br/> |<span data-ttu-id="47182-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="47182-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47182-109">Définition</span><span class="sxs-lookup"><span data-stu-id="47182-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="47182-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="47182-110">Elements and attributes</span></span>

<span data-ttu-id="47182-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="47182-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="47182-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="47182-112">Child elements</span></span>

<span data-ttu-id="47182-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="47182-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47182-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="47182-114">Attributes</span></span>

|<span data-ttu-id="47182-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="47182-115">**Attribute**</span></span>|<span data-ttu-id="47182-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="47182-116">**Type**</span></span>|<span data-ttu-id="47182-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="47182-117">**Required**</span></span>|<span data-ttu-id="47182-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="47182-118">**Description**</span></span>|<span data-ttu-id="47182-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="47182-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="47182-120">Jeu de caractères</span><span class="sxs-lookup"><span data-stu-id="47182-120">CharSet</span></span>  <br/> |<span data-ttu-id="47182-121">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="47182-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="47182-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-122">optional</span></span>  <br/> ||<span data-ttu-id="47182-123">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="47182-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="47182-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="47182-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="47182-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="47182-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="47182-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-126">optional</span></span>  <br/> ||<span data-ttu-id="47182-127">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="47182-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="47182-128">Échappement</span><span class="sxs-lookup"><span data-stu-id="47182-128">Escapement</span></span>  <br/> |<span data-ttu-id="47182-129">XSD : int</span><span class="sxs-lookup"><span data-stu-id="47182-129">xsd:int</span></span>  <br/> |<span data-ttu-id="47182-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-130">optional</span></span>  <br/> ||<span data-ttu-id="47182-131">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="47182-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="47182-132">Nom de la police</span><span class="sxs-lookup"><span data-stu-id="47182-132">FaceName</span></span>  <br/> |<span data-ttu-id="47182-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="47182-133">xsd:string</span></span>  <br/> |<span data-ttu-id="47182-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-134">optional</span></span>  <br/> ||<span data-ttu-id="47182-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="47182-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="47182-136">Height</span><span class="sxs-lookup"><span data-stu-id="47182-136">Height</span></span>  <br/> |<span data-ttu-id="47182-137">XSD : int</span><span class="sxs-lookup"><span data-stu-id="47182-137">xsd:int</span></span>  <br/> |<span data-ttu-id="47182-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-138">optional</span></span>  <br/> ||<span data-ttu-id="47182-139">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="47182-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="47182-140">Italique</span><span class="sxs-lookup"><span data-stu-id="47182-140">Italic</span></span>  <br/> |<span data-ttu-id="47182-141">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="47182-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="47182-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-142">optional</span></span>  <br/> ||<span data-ttu-id="47182-143">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="47182-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="47182-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="47182-144">Orientation</span></span>  <br/> |<span data-ttu-id="47182-145">XSD : int</span><span class="sxs-lookup"><span data-stu-id="47182-145">xsd:int</span></span>  <br/> |<span data-ttu-id="47182-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-146">optional</span></span>  <br/> ||<span data-ttu-id="47182-147">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="47182-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="47182-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="47182-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="47182-149">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="47182-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="47182-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-150">optional</span></span>  <br/> ||<span data-ttu-id="47182-151">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="47182-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="47182-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="47182-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="47182-153">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="47182-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="47182-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-154">optional</span></span>  <br/> ||<span data-ttu-id="47182-155">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="47182-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="47182-156">Qualité</span><span class="sxs-lookup"><span data-stu-id="47182-156">Quality</span></span>  <br/> |<span data-ttu-id="47182-157">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="47182-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="47182-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-158">optional</span></span>  <br/> ||<span data-ttu-id="47182-159">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="47182-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="47182-160">Barré</span><span class="sxs-lookup"><span data-stu-id="47182-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="47182-161">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="47182-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="47182-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-162">optional</span></span>  <br/> ||<span data-ttu-id="47182-163">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="47182-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="47182-164">Souligné</span><span class="sxs-lookup"><span data-stu-id="47182-164">Underline</span></span>  <br/> |<span data-ttu-id="47182-165">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="47182-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="47182-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-166">optional</span></span>  <br/> ||<span data-ttu-id="47182-167">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="47182-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="47182-168">Pondération</span><span class="sxs-lookup"><span data-stu-id="47182-168">Weight</span></span>  <br/> |<span data-ttu-id="47182-169">XSD : int</span><span class="sxs-lookup"><span data-stu-id="47182-169">xsd:int</span></span>  <br/> |<span data-ttu-id="47182-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-170">optional</span></span>  <br/> ||<span data-ttu-id="47182-171">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="47182-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="47182-172">Width</span><span class="sxs-lookup"><span data-stu-id="47182-172">Width</span></span>  <br/> |<span data-ttu-id="47182-173">XSD : int</span><span class="sxs-lookup"><span data-stu-id="47182-173">xsd:int</span></span>  <br/> |<span data-ttu-id="47182-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="47182-174">optional</span></span>  <br/> ||<span data-ttu-id="47182-175">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="47182-175">Values of the xsd:int type.</span></span>  <br/> |
   

