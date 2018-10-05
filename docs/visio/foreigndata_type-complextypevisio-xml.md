---
title: Type complexe ForeignData_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384156"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="178fb-102">Type complexe ForeignData_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="178fb-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="178fb-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="178fb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="178fb-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="178fb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="178fb-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="178fb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="178fb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="178fb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="178fb-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="178fb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="178fb-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="178fb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="178fb-109">Définition</span><span class="sxs-lookup"><span data-stu-id="178fb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="178fb-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="178fb-110">Elements and attributes</span></span>

<span data-ttu-id="178fb-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="178fb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="178fb-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="178fb-112">Child elements</span></span>

|<span data-ttu-id="178fb-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="178fb-113">**Element**</span></span>|<span data-ttu-id="178fb-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="178fb-114">**Type**</span></span>|<span data-ttu-id="178fb-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="178fb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="178fb-116">Rel</span><span class="sxs-lookup"><span data-stu-id="178fb-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="178fb-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="178fb-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="178fb-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="178fb-118">Attributes</span></span>

|<span data-ttu-id="178fb-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="178fb-119">**Attribute**</span></span>|<span data-ttu-id="178fb-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="178fb-120">**Type**</span></span>|<span data-ttu-id="178fb-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="178fb-121">**Required**</span></span>|<span data-ttu-id="178fb-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="178fb-122">**Description**</span></span>|<span data-ttu-id="178fb-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="178fb-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="178fb-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="178fb-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="178fb-125">XSD : double</span><span class="sxs-lookup"><span data-stu-id="178fb-125">xsd:double</span></span>  <br/> |<span data-ttu-id="178fb-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="178fb-126">optional</span></span>  <br/> ||<span data-ttu-id="178fb-127">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="178fb-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="178fb-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="178fb-128">CompressionType</span></span>  <br/> |<span data-ttu-id="178fb-129">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="178fb-129">xsd:token</span></span>  <br/> |<span data-ttu-id="178fb-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="178fb-130">optional</span></span>  <br/> ||<span data-ttu-id="178fb-131">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="178fb-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="178fb-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="178fb-132">ExtentX</span></span>  <br/> |<span data-ttu-id="178fb-133">XSD : double</span><span class="sxs-lookup"><span data-stu-id="178fb-133">xsd:double</span></span>  <br/> |<span data-ttu-id="178fb-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="178fb-134">optional</span></span>  <br/> ||<span data-ttu-id="178fb-135">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="178fb-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="178fb-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="178fb-136">ExtentY</span></span>  <br/> |<span data-ttu-id="178fb-137">XSD : double</span><span class="sxs-lookup"><span data-stu-id="178fb-137">xsd:double</span></span>  <br/> |<span data-ttu-id="178fb-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="178fb-138">optional</span></span>  <br/> ||<span data-ttu-id="178fb-139">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="178fb-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="178fb-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="178fb-140">ForeignType</span></span>  <br/> |<span data-ttu-id="178fb-141">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="178fb-141">xsd:token</span></span>  <br/> |<span data-ttu-id="178fb-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="178fb-142">required</span></span>  <br/> ||<span data-ttu-id="178fb-143">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="178fb-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="178fb-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="178fb-144">MappingMode</span></span>  <br/> |<span data-ttu-id="178fb-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="178fb-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="178fb-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="178fb-146">optional</span></span>  <br/> ||<span data-ttu-id="178fb-147">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="178fb-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="178fb-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="178fb-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="178fb-149">XSD : double</span><span class="sxs-lookup"><span data-stu-id="178fb-149">xsd:double</span></span>  <br/> |<span data-ttu-id="178fb-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="178fb-150">optional</span></span>  <br/> ||<span data-ttu-id="178fb-151">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="178fb-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="178fb-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="178fb-152">ObjectType</span></span>  <br/> |<span data-ttu-id="178fb-153">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="178fb-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="178fb-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="178fb-154">optional</span></span>  <br/> ||<span data-ttu-id="178fb-155">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="178fb-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="178fb-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="178fb-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="178fb-157">XSD : double</span><span class="sxs-lookup"><span data-stu-id="178fb-157">xsd:double</span></span>  <br/> |<span data-ttu-id="178fb-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="178fb-158">optional</span></span>  <br/> ||<span data-ttu-id="178fb-159">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="178fb-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="178fb-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="178fb-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="178fb-161">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="178fb-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="178fb-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="178fb-162">optional</span></span>  <br/> ||<span data-ttu-id="178fb-163">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="178fb-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

