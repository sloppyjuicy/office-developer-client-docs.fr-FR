---
title: ShapeSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 0094bc9643cc1331e0b47bd11a59769a553e17f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542057"
---
# <a name="shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="e0b48-102">ShapeSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e0b48-102">ShapeSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e0b48-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="e0b48-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0b48-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e0b48-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e0b48-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e0b48-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e0b48-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e0b48-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e0b48-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="e0b48-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e0b48-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="e0b48-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e0b48-109">Définition</span><span class="sxs-lookup"><span data-stu-id="e0b48-109">Definition</span></span>

```XML
          <xs:complexType name="ShapeSheet_Type">
          
          <xs:complexContent>
          <xs:extension base="Sheet_Type">
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Text"  type="Text_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data1"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data2"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data3"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ForeignData"  type="ForeignData_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="OriginalID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="MasterShape"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Type"
  type="xsd:token"
    />
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e0b48-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e0b48-110">Elements and attributes</span></span>

<span data-ttu-id="e0b48-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="e0b48-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e0b48-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e0b48-112">Child elements</span></span>

|<span data-ttu-id="e0b48-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e0b48-113">**Element**</span></span>|<span data-ttu-id="e0b48-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="e0b48-114">**Type**</span></span>|<span data-ttu-id="e0b48-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="e0b48-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e0b48-116">Data1</span><span class="sxs-lookup"><span data-stu-id="e0b48-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0b48-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="e0b48-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0b48-118">Data2</span><span class="sxs-lookup"><span data-stu-id="e0b48-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0b48-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="e0b48-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0b48-120">Data3</span><span class="sxs-lookup"><span data-stu-id="e0b48-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0b48-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="e0b48-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0b48-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="e0b48-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0b48-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="e0b48-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0b48-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="e0b48-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0b48-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="e0b48-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0b48-126">Texte</span><span class="sxs-lookup"><span data-stu-id="e0b48-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0b48-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="e0b48-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e0b48-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="e0b48-128">Attributes</span></span>

|<span data-ttu-id="e0b48-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e0b48-129">**Attribute**</span></span>|<span data-ttu-id="e0b48-130">**Type**</span><span class="sxs-lookup"><span data-stu-id="e0b48-130">**Type**</span></span>|<span data-ttu-id="e0b48-131">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e0b48-131">**Required**</span></span>|<span data-ttu-id="e0b48-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="e0b48-132">**Description**</span></span>|<span data-ttu-id="e0b48-133">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e0b48-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e0b48-134">Del</span><span class="sxs-lookup"><span data-stu-id="e0b48-134">Del</span></span>  <br/> |<span data-ttu-id="e0b48-135">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e0b48-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e0b48-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0b48-136">optional</span></span>  <br/> ||<span data-ttu-id="e0b48-137">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e0b48-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e0b48-138">ID</span><span class="sxs-lookup"><span data-stu-id="e0b48-138">ID</span></span>  <br/> |<span data-ttu-id="e0b48-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e0b48-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0b48-140">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e0b48-140">required</span></span>  <br/> ||<span data-ttu-id="e0b48-141">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e0b48-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0b48-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="e0b48-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="e0b48-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e0b48-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e0b48-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0b48-144">optional</span></span>  <br/> ||<span data-ttu-id="e0b48-145">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e0b48-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e0b48-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="e0b48-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="e0b48-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e0b48-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e0b48-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0b48-148">optional</span></span>  <br/> ||<span data-ttu-id="e0b48-149">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e0b48-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e0b48-150">Master</span><span class="sxs-lookup"><span data-stu-id="e0b48-150">Master</span></span>  <br/> |<span data-ttu-id="e0b48-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e0b48-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0b48-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0b48-152">optional</span></span>  <br/> ||<span data-ttu-id="e0b48-153">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e0b48-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0b48-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="e0b48-154">MasterShape</span></span>  <br/> |<span data-ttu-id="e0b48-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e0b48-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0b48-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0b48-156">optional</span></span>  <br/> ||<span data-ttu-id="e0b48-157">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e0b48-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0b48-158">Nom</span><span class="sxs-lookup"><span data-stu-id="e0b48-158">Name</span></span>  <br/> |<span data-ttu-id="e0b48-159">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e0b48-159">xsd:string</span></span>  <br/> |<span data-ttu-id="e0b48-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0b48-160">optional</span></span>  <br/> ||<span data-ttu-id="e0b48-161">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e0b48-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e0b48-162">NameU</span><span class="sxs-lookup"><span data-stu-id="e0b48-162">NameU</span></span>  <br/> |<span data-ttu-id="e0b48-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e0b48-163">xsd:string</span></span>  <br/> |<span data-ttu-id="e0b48-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0b48-164">optional</span></span>  <br/> ||<span data-ttu-id="e0b48-165">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e0b48-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e0b48-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="e0b48-166">OriginalID</span></span>  <br/> |<span data-ttu-id="e0b48-167">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e0b48-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0b48-168">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0b48-168">optional</span></span>  <br/> ||<span data-ttu-id="e0b48-169">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e0b48-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0b48-170">Type</span><span class="sxs-lookup"><span data-stu-id="e0b48-170">Type</span></span>  <br/> |<span data-ttu-id="e0b48-171">xsd:token</span><span class="sxs-lookup"><span data-stu-id="e0b48-171">xsd:token</span></span>  <br/> |<span data-ttu-id="e0b48-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0b48-172">optional</span></span>  <br/> ||<span data-ttu-id="e0b48-173">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="e0b48-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="e0b48-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="e0b48-174">UniqueID</span></span>  <br/> |<span data-ttu-id="e0b48-175">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e0b48-175">xsd:string</span></span>  <br/> |<span data-ttu-id="e0b48-176">facultatif</span><span class="sxs-lookup"><span data-stu-id="e0b48-176">optional</span></span>  <br/> ||<span data-ttu-id="e0b48-177">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e0b48-177">Values of the xsd:string type.</span></span>  <br/> |
   

