---
title: ComplexType ForeignData_Type (Visio XML)
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
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="69552-102">ComplexType ForeignData_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="69552-102">ForeignData_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="69552-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="69552-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69552-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="69552-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="69552-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="69552-105">**Schema file**</span></span> <br/> |<span data-ttu-id="69552-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="69552-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="69552-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="69552-107">**Extension base**</span></span> <br/> |<span data-ttu-id="69552-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="69552-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="69552-109">Définition</span><span class="sxs-lookup"><span data-stu-id="69552-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="69552-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="69552-110">Elements and attributes</span></span>

<span data-ttu-id="69552-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="69552-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="69552-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="69552-112">Child elements</span></span>

|<span data-ttu-id="69552-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="69552-113">**Element**</span></span>|<span data-ttu-id="69552-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="69552-114">**Type**</span></span>|<span data-ttu-id="69552-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="69552-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="69552-116">Ver</span><span class="sxs-lookup"><span data-stu-id="69552-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="69552-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="69552-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="69552-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="69552-118">Attributes</span></span>

|<span data-ttu-id="69552-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="69552-119">**Attribute**</span></span>|<span data-ttu-id="69552-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="69552-120">**Type**</span></span>|<span data-ttu-id="69552-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="69552-121">**Required**</span></span>|<span data-ttu-id="69552-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="69552-122">**Description**</span></span>|<span data-ttu-id="69552-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="69552-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="69552-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="69552-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="69552-125">xsd: double</span><span class="sxs-lookup"><span data-stu-id="69552-125">xsd:double</span></span>  <br/> |<span data-ttu-id="69552-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="69552-126">optional</span></span>  <br/> ||<span data-ttu-id="69552-127">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="69552-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="69552-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="69552-128">CompressionType</span></span>  <br/> |<span data-ttu-id="69552-129">xsd: Token</span><span class="sxs-lookup"><span data-stu-id="69552-129">xsd:token</span></span>  <br/> |<span data-ttu-id="69552-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="69552-130">optional</span></span>  <br/> ||<span data-ttu-id="69552-131">Valeurs du type xsd: Token.</span><span class="sxs-lookup"><span data-stu-id="69552-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="69552-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="69552-132">ExtentX</span></span>  <br/> |<span data-ttu-id="69552-133">xsd: double</span><span class="sxs-lookup"><span data-stu-id="69552-133">xsd:double</span></span>  <br/> |<span data-ttu-id="69552-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="69552-134">optional</span></span>  <br/> ||<span data-ttu-id="69552-135">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="69552-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="69552-136">Étendue</span><span class="sxs-lookup"><span data-stu-id="69552-136">ExtentY</span></span>  <br/> |<span data-ttu-id="69552-137">xsd: double</span><span class="sxs-lookup"><span data-stu-id="69552-137">xsd:double</span></span>  <br/> |<span data-ttu-id="69552-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="69552-138">optional</span></span>  <br/> ||<span data-ttu-id="69552-139">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="69552-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="69552-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="69552-140">ForeignType</span></span>  <br/> |<span data-ttu-id="69552-141">xsd: Token</span><span class="sxs-lookup"><span data-stu-id="69552-141">xsd:token</span></span>  <br/> |<span data-ttu-id="69552-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="69552-142">required</span></span>  <br/> ||<span data-ttu-id="69552-143">Valeurs du type xsd: Token.</span><span class="sxs-lookup"><span data-stu-id="69552-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="69552-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="69552-144">MappingMode</span></span>  <br/> |<span data-ttu-id="69552-145">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="69552-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="69552-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="69552-146">optional</span></span>  <br/> ||<span data-ttu-id="69552-147">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="69552-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="69552-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="69552-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="69552-149">xsd: double</span><span class="sxs-lookup"><span data-stu-id="69552-149">xsd:double</span></span>  <br/> |<span data-ttu-id="69552-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="69552-150">optional</span></span>  <br/> ||<span data-ttu-id="69552-151">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="69552-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="69552-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="69552-152">ObjectType</span></span>  <br/> |<span data-ttu-id="69552-153">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69552-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69552-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="69552-154">optional</span></span>  <br/> ||<span data-ttu-id="69552-155">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="69552-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69552-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="69552-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="69552-157">xsd: double</span><span class="sxs-lookup"><span data-stu-id="69552-157">xsd:double</span></span>  <br/> |<span data-ttu-id="69552-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="69552-158">optional</span></span>  <br/> ||<span data-ttu-id="69552-159">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="69552-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="69552-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="69552-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="69552-161">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="69552-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="69552-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="69552-162">optional</span></span>  <br/> ||<span data-ttu-id="69552-163">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="69552-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

