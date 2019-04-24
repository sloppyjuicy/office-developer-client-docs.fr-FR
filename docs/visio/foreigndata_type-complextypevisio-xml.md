---
title: ComplexType ForeignData_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346010"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="a64a8-102">ComplexType ForeignData_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="a64a8-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a64a8-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a64a8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a64a8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a64a8-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a64a8-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a64a8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a64a8-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a64a8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a64a8-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a64a8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a64a8-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="a64a8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a64a8-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a64a8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a64a8-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a64a8-110">Elements and attributes</span></span>

<span data-ttu-id="a64a8-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="a64a8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a64a8-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a64a8-112">Child elements</span></span>

|<span data-ttu-id="a64a8-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a64a8-113">**Element**</span></span>|<span data-ttu-id="a64a8-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="a64a8-114">**Type**</span></span>|<span data-ttu-id="a64a8-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a64a8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a64a8-116">Ver</span><span class="sxs-lookup"><span data-stu-id="a64a8-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a64a8-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="a64a8-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a64a8-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="a64a8-118">Attributes</span></span>

|<span data-ttu-id="a64a8-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a64a8-119">**Attribute**</span></span>|<span data-ttu-id="a64a8-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="a64a8-120">**Type**</span></span>|<span data-ttu-id="a64a8-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a64a8-121">**Required**</span></span>|<span data-ttu-id="a64a8-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="a64a8-122">**Description**</span></span>|<span data-ttu-id="a64a8-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a64a8-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a64a8-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="a64a8-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="a64a8-125">xsd: double</span><span class="sxs-lookup"><span data-stu-id="a64a8-125">xsd:double</span></span>  <br/> |<span data-ttu-id="a64a8-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="a64a8-126">optional</span></span>  <br/> ||<span data-ttu-id="a64a8-127">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="a64a8-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a64a8-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="a64a8-128">CompressionType</span></span>  <br/> |<span data-ttu-id="a64a8-129">xsd: Token</span><span class="sxs-lookup"><span data-stu-id="a64a8-129">xsd:token</span></span>  <br/> |<span data-ttu-id="a64a8-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="a64a8-130">optional</span></span>  <br/> ||<span data-ttu-id="a64a8-131">Valeurs du type xsd: Token.</span><span class="sxs-lookup"><span data-stu-id="a64a8-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a64a8-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="a64a8-132">ExtentX</span></span>  <br/> |<span data-ttu-id="a64a8-133">xsd: double</span><span class="sxs-lookup"><span data-stu-id="a64a8-133">xsd:double</span></span>  <br/> |<span data-ttu-id="a64a8-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="a64a8-134">optional</span></span>  <br/> ||<span data-ttu-id="a64a8-135">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="a64a8-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a64a8-136">Étendue</span><span class="sxs-lookup"><span data-stu-id="a64a8-136">ExtentY</span></span>  <br/> |<span data-ttu-id="a64a8-137">xsd: double</span><span class="sxs-lookup"><span data-stu-id="a64a8-137">xsd:double</span></span>  <br/> |<span data-ttu-id="a64a8-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="a64a8-138">optional</span></span>  <br/> ||<span data-ttu-id="a64a8-139">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="a64a8-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a64a8-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="a64a8-140">ForeignType</span></span>  <br/> |<span data-ttu-id="a64a8-141">xsd: Token</span><span class="sxs-lookup"><span data-stu-id="a64a8-141">xsd:token</span></span>  <br/> |<span data-ttu-id="a64a8-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a64a8-142">required</span></span>  <br/> ||<span data-ttu-id="a64a8-143">Valeurs du type xsd: Token.</span><span class="sxs-lookup"><span data-stu-id="a64a8-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a64a8-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="a64a8-144">MappingMode</span></span>  <br/> |<span data-ttu-id="a64a8-145">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a64a8-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a64a8-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="a64a8-146">optional</span></span>  <br/> ||<span data-ttu-id="a64a8-147">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a64a8-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a64a8-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="a64a8-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="a64a8-149">xsd: double</span><span class="sxs-lookup"><span data-stu-id="a64a8-149">xsd:double</span></span>  <br/> |<span data-ttu-id="a64a8-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="a64a8-150">optional</span></span>  <br/> ||<span data-ttu-id="a64a8-151">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="a64a8-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a64a8-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="a64a8-152">ObjectType</span></span>  <br/> |<span data-ttu-id="a64a8-153">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a64a8-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a64a8-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="a64a8-154">optional</span></span>  <br/> ||<span data-ttu-id="a64a8-155">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a64a8-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a64a8-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="a64a8-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="a64a8-157">xsd: double</span><span class="sxs-lookup"><span data-stu-id="a64a8-157">xsd:double</span></span>  <br/> |<span data-ttu-id="a64a8-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="a64a8-158">optional</span></span>  <br/> ||<span data-ttu-id="a64a8-159">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="a64a8-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a64a8-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="a64a8-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="a64a8-161">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="a64a8-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a64a8-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="a64a8-162">optional</span></span>  <br/> ||<span data-ttu-id="a64a8-163">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a64a8-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

