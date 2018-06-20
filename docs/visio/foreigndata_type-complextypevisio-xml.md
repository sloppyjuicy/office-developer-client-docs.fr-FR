---
title: Type complexe ForeignData_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 1d9358de2f88a1b9e035ecf4966544ea935f8b2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788688"
---
# <a name="foreigndatatype-complextype-visio-xml"></a><span data-ttu-id="c919e-102">Type complexe ForeignData_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="c919e-102">ForeignData_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c919e-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c919e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c919e-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c919e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c919e-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c919e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c919e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c919e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c919e-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c919e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c919e-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="c919e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c919e-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c919e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c919e-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c919e-110">Elements and attributes</span></span>

<span data-ttu-id="c919e-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c919e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c919e-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c919e-112">Child elements</span></span>

|<span data-ttu-id="c919e-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c919e-113">**Element**</span></span>|<span data-ttu-id="c919e-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="c919e-114">**Type**</span></span>|<span data-ttu-id="c919e-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="c919e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c919e-116">Rel</span><span class="sxs-lookup"><span data-stu-id="c919e-116">Rel</span></span>](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c919e-117">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="c919e-117">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c919e-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="c919e-118">Attributes</span></span>

|<span data-ttu-id="c919e-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c919e-119">**Attribute**</span></span>|<span data-ttu-id="c919e-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="c919e-120">**Type**</span></span>|<span data-ttu-id="c919e-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c919e-121">**Required**</span></span>|<span data-ttu-id="c919e-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="c919e-122">**Description**</span></span>|<span data-ttu-id="c919e-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c919e-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c919e-124">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="c919e-124">CompressionLevel</span></span>  <br/> |<span data-ttu-id="c919e-125">XSD : double</span><span class="sxs-lookup"><span data-stu-id="c919e-125">xsd:double</span></span>  <br/> |<span data-ttu-id="c919e-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="c919e-126">optional</span></span>  <br/> ||<span data-ttu-id="c919e-127">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="c919e-127">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c919e-128">CompressionType</span><span class="sxs-lookup"><span data-stu-id="c919e-128">CompressionType</span></span>  <br/> |<span data-ttu-id="c919e-129">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="c919e-129">xsd:token</span></span>  <br/> |<span data-ttu-id="c919e-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="c919e-130">optional</span></span>  <br/> ||<span data-ttu-id="c919e-131">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="c919e-131">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="c919e-132">ExtentX</span><span class="sxs-lookup"><span data-stu-id="c919e-132">ExtentX</span></span>  <br/> |<span data-ttu-id="c919e-133">XSD : double</span><span class="sxs-lookup"><span data-stu-id="c919e-133">xsd:double</span></span>  <br/> |<span data-ttu-id="c919e-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="c919e-134">optional</span></span>  <br/> ||<span data-ttu-id="c919e-135">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="c919e-135">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c919e-136">ExtentY</span><span class="sxs-lookup"><span data-stu-id="c919e-136">ExtentY</span></span>  <br/> |<span data-ttu-id="c919e-137">XSD : double</span><span class="sxs-lookup"><span data-stu-id="c919e-137">xsd:double</span></span>  <br/> |<span data-ttu-id="c919e-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="c919e-138">optional</span></span>  <br/> ||<span data-ttu-id="c919e-139">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="c919e-139">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c919e-140">ForeignType</span><span class="sxs-lookup"><span data-stu-id="c919e-140">ForeignType</span></span>  <br/> |<span data-ttu-id="c919e-141">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="c919e-141">xsd:token</span></span>  <br/> |<span data-ttu-id="c919e-142">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c919e-142">required</span></span>  <br/> ||<span data-ttu-id="c919e-143">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="c919e-143">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="c919e-144">MappingMode</span><span class="sxs-lookup"><span data-stu-id="c919e-144">MappingMode</span></span>  <br/> |<span data-ttu-id="c919e-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c919e-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c919e-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="c919e-146">optional</span></span>  <br/> ||<span data-ttu-id="c919e-147">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c919e-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c919e-148">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="c919e-148">ObjectHeight</span></span>  <br/> |<span data-ttu-id="c919e-149">XSD : double</span><span class="sxs-lookup"><span data-stu-id="c919e-149">xsd:double</span></span>  <br/> |<span data-ttu-id="c919e-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="c919e-150">optional</span></span>  <br/> ||<span data-ttu-id="c919e-151">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="c919e-151">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c919e-152">ObjectType</span><span class="sxs-lookup"><span data-stu-id="c919e-152">ObjectType</span></span>  <br/> |<span data-ttu-id="c919e-153">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c919e-153">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c919e-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="c919e-154">optional</span></span>  <br/> ||<span data-ttu-id="c919e-155">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c919e-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c919e-156">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="c919e-156">ObjectWidth</span></span>  <br/> |<span data-ttu-id="c919e-157">XSD : double</span><span class="sxs-lookup"><span data-stu-id="c919e-157">xsd:double</span></span>  <br/> |<span data-ttu-id="c919e-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="c919e-158">optional</span></span>  <br/> ||<span data-ttu-id="c919e-159">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="c919e-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="c919e-160">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="c919e-160">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="c919e-161">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="c919e-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c919e-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="c919e-162">optional</span></span>  <br/> ||<span data-ttu-id="c919e-163">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="c919e-163">Values of the xsd:boolean type.</span></span>  <br/> |
   

