---
title: Type complexe HeaderFooterFont_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397246"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="cdbcf-102">Type complexe HeaderFooterFont_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="cdbcf-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cdbcf-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="cdbcf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdbcf-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="cdbcf-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cdbcf-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="cdbcf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cdbcf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cdbcf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cdbcf-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="cdbcf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cdbcf-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="cdbcf-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cdbcf-109">Définition</span><span class="sxs-lookup"><span data-stu-id="cdbcf-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cdbcf-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="cdbcf-110">Elements and attributes</span></span>

<span data-ttu-id="cdbcf-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cdbcf-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cdbcf-112">Child elements</span></span>

<span data-ttu-id="cdbcf-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cdbcf-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="cdbcf-114">Attributes</span></span>

|<span data-ttu-id="cdbcf-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cdbcf-115">**Attribute**</span></span>|<span data-ttu-id="cdbcf-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="cdbcf-116">**Type**</span></span>|<span data-ttu-id="cdbcf-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="cdbcf-117">**Required**</span></span>|<span data-ttu-id="cdbcf-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="cdbcf-118">**Description**</span></span>|<span data-ttu-id="cdbcf-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="cdbcf-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cdbcf-120">Jeu de caractères</span><span class="sxs-lookup"><span data-stu-id="cdbcf-120">CharSet</span></span>  <br/> |<span data-ttu-id="cdbcf-121">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="cdbcf-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="cdbcf-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-122">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-123">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="cdbcf-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="cdbcf-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="cdbcf-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="cdbcf-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-126">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-127">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-128">Échappement</span><span class="sxs-lookup"><span data-stu-id="cdbcf-128">Escapement</span></span>  <br/> |<span data-ttu-id="cdbcf-129">XSD : int</span><span class="sxs-lookup"><span data-stu-id="cdbcf-129">xsd:int</span></span>  <br/> |<span data-ttu-id="cdbcf-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-130">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-131">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-132">Nom de la police</span><span class="sxs-lookup"><span data-stu-id="cdbcf-132">FaceName</span></span>  <br/> |<span data-ttu-id="cdbcf-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="cdbcf-133">xsd:string</span></span>  <br/> |<span data-ttu-id="cdbcf-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-134">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-136">Height</span><span class="sxs-lookup"><span data-stu-id="cdbcf-136">Height</span></span>  <br/> |<span data-ttu-id="cdbcf-137">XSD : int</span><span class="sxs-lookup"><span data-stu-id="cdbcf-137">xsd:int</span></span>  <br/> |<span data-ttu-id="cdbcf-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-138">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-139">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-140">Italique</span><span class="sxs-lookup"><span data-stu-id="cdbcf-140">Italic</span></span>  <br/> |<span data-ttu-id="cdbcf-141">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="cdbcf-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="cdbcf-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-142">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-143">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-144">Orientation</span><span class="sxs-lookup"><span data-stu-id="cdbcf-144">Orientation</span></span>  <br/> |<span data-ttu-id="cdbcf-145">XSD : int</span><span class="sxs-lookup"><span data-stu-id="cdbcf-145">xsd:int</span></span>  <br/> |<span data-ttu-id="cdbcf-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-146">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-147">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="cdbcf-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="cdbcf-149">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="cdbcf-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="cdbcf-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-150">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-151">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="cdbcf-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="cdbcf-153">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="cdbcf-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="cdbcf-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-154">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-155">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-156">Qualité</span><span class="sxs-lookup"><span data-stu-id="cdbcf-156">Quality</span></span>  <br/> |<span data-ttu-id="cdbcf-157">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="cdbcf-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="cdbcf-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-158">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-159">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-160">Barré</span><span class="sxs-lookup"><span data-stu-id="cdbcf-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="cdbcf-161">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="cdbcf-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="cdbcf-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-162">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-163">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-164">Souligné</span><span class="sxs-lookup"><span data-stu-id="cdbcf-164">Underline</span></span>  <br/> |<span data-ttu-id="cdbcf-165">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="cdbcf-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="cdbcf-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-166">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-167">Valeurs du type xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-168">Pondération</span><span class="sxs-lookup"><span data-stu-id="cdbcf-168">Weight</span></span>  <br/> |<span data-ttu-id="cdbcf-169">XSD : int</span><span class="sxs-lookup"><span data-stu-id="cdbcf-169">xsd:int</span></span>  <br/> |<span data-ttu-id="cdbcf-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-170">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-171">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="cdbcf-172">Width</span><span class="sxs-lookup"><span data-stu-id="cdbcf-172">Width</span></span>  <br/> |<span data-ttu-id="cdbcf-173">XSD : int</span><span class="sxs-lookup"><span data-stu-id="cdbcf-173">xsd:int</span></span>  <br/> |<span data-ttu-id="cdbcf-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="cdbcf-174">optional</span></span>  <br/> ||<span data-ttu-id="cdbcf-175">Valeurs du type xsd : int.</span><span class="sxs-lookup"><span data-stu-id="cdbcf-175">Values of the xsd:int type.</span></span>  <br/> |
   

