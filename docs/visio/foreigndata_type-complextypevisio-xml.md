---
title: ForeignData_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 39396ef0db5b78d6f32d8828103eecd105f8b91d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539862"
---
# <a name="foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="6046b-102">ForeignData_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6046b-102">ForeignData_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6046b-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="6046b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6046b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6046b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6046b-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6046b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6046b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6046b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6046b-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="6046b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6046b-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="6046b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6046b-109">Définition</span><span class="sxs-lookup"><span data-stu-id="6046b-109">Definition</span></span>

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6046b-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6046b-110">Elements and attributes</span></span>

<span data-ttu-id="6046b-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="6046b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6046b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6046b-112">Child elements</span></span>

|<span data-ttu-id="6046b-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6046b-113">**Element**</span></span>|<span data-ttu-id="6046b-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="6046b-114">**Type**</span></span>|<span data-ttu-id="6046b-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="6046b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6046b-116">Rel</span><span class="sxs-lookup"><span data-stu-id="6046b-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6046b-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="6046b-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6046b-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="6046b-118">Attributes</span></span>

|<span data-ttu-id="6046b-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6046b-119">**Attribute**</span></span>|<span data-ttu-id="6046b-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="6046b-120">**Type**</span></span>|<span data-ttu-id="6046b-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="6046b-121">**Required**</span></span>|<span data-ttu-id="6046b-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="6046b-122">**Description**</span></span>|<span data-ttu-id="6046b-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="6046b-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6046b-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="6046b-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="6046b-125">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6046b-125">xsd:double</span></span>  <br/> |<span data-ttu-id="6046b-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="6046b-126">optional</span></span>  <br/> ||<span data-ttu-id="6046b-127">Valeurs du type xsd:double.</span><span class="sxs-lookup"><span data-stu-id="6046b-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6046b-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="6046b-128">CompressionType</span></span>  <br/> |<span data-ttu-id="6046b-129">xsd:token</span><span class="sxs-lookup"><span data-stu-id="6046b-129">xsd:token</span></span>  <br/> |<span data-ttu-id="6046b-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="6046b-130">optional</span></span>  <br/> ||<span data-ttu-id="6046b-131">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="6046b-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="6046b-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="6046b-132">ExtentX</span></span>  <br/> |<span data-ttu-id="6046b-133">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6046b-133">xsd:double</span></span>  <br/> |<span data-ttu-id="6046b-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="6046b-134">optional</span></span>  <br/> ||<span data-ttu-id="6046b-135">Valeurs du type xsd:double.</span><span class="sxs-lookup"><span data-stu-id="6046b-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6046b-136">Extenty</span><span class="sxs-lookup"><span data-stu-id="6046b-136">ExtentY</span></span>  <br/> |<span data-ttu-id="6046b-137">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6046b-137">xsd:double</span></span>  <br/> |<span data-ttu-id="6046b-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="6046b-138">optional</span></span>  <br/> ||<span data-ttu-id="6046b-139">Valeurs du type xsd:double.</span><span class="sxs-lookup"><span data-stu-id="6046b-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6046b-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="6046b-140">ForeignType</span></span>  <br/> |<span data-ttu-id="6046b-141">xsd:token</span><span class="sxs-lookup"><span data-stu-id="6046b-141">xsd:token</span></span>  <br/> |<span data-ttu-id="6046b-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="6046b-142">required</span></span>  <br/> ||<span data-ttu-id="6046b-143">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="6046b-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="6046b-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="6046b-144">MappingMode</span></span>  <br/> |<span data-ttu-id="6046b-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6046b-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="6046b-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="6046b-146">optional</span></span>  <br/> ||<span data-ttu-id="6046b-147">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="6046b-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="6046b-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="6046b-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="6046b-149">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6046b-149">xsd:double</span></span>  <br/> |<span data-ttu-id="6046b-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="6046b-150">optional</span></span>  <br/> ||<span data-ttu-id="6046b-151">Valeurs du type xsd:double.</span><span class="sxs-lookup"><span data-stu-id="6046b-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6046b-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="6046b-152">ObjectType</span></span>  <br/> |<span data-ttu-id="6046b-153">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6046b-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6046b-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="6046b-154">optional</span></span>  <br/> ||<span data-ttu-id="6046b-155">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6046b-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6046b-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="6046b-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="6046b-157">xsd:double</span><span class="sxs-lookup"><span data-stu-id="6046b-157">xsd:double</span></span>  <br/> |<span data-ttu-id="6046b-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="6046b-158">optional</span></span>  <br/> ||<span data-ttu-id="6046b-159">Valeurs du type xsd:double.</span><span class="sxs-lookup"><span data-stu-id="6046b-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="6046b-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="6046b-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="6046b-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6046b-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6046b-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="6046b-162">optional</span></span>  <br/> ||<span data-ttu-id="6046b-163">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6046b-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

