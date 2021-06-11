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
# <a name="shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="9a601-102">ShapeSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9a601-102">ShapeSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9a601-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9a601-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a601-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9a601-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9a601-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9a601-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9a601-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9a601-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9a601-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9a601-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9a601-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="9a601-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a601-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9a601-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9a601-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9a601-110">Elements and attributes</span></span>

<span data-ttu-id="9a601-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="9a601-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9a601-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9a601-112">Child elements</span></span>

|<span data-ttu-id="9a601-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9a601-113">**Element**</span></span>|<span data-ttu-id="9a601-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="9a601-114">**Type**</span></span>|<span data-ttu-id="9a601-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9a601-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9a601-116">Data1</span><span class="sxs-lookup"><span data-stu-id="9a601-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a601-117">Data_Type</span><span class="sxs-lookup"><span data-stu-id="9a601-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a601-118">Data2</span><span class="sxs-lookup"><span data-stu-id="9a601-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a601-119">Data_Type</span><span class="sxs-lookup"><span data-stu-id="9a601-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a601-120">Data3</span><span class="sxs-lookup"><span data-stu-id="9a601-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a601-121">Data_Type</span><span class="sxs-lookup"><span data-stu-id="9a601-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a601-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="9a601-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a601-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="9a601-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a601-124">Formes</span><span class="sxs-lookup"><span data-stu-id="9a601-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a601-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="9a601-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a601-126">Text</span><span class="sxs-lookup"><span data-stu-id="9a601-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a601-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="9a601-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9a601-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="9a601-128">Attributes</span></span>

|<span data-ttu-id="9a601-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9a601-129">**Attribute**</span></span>|<span data-ttu-id="9a601-130">**Type**</span><span class="sxs-lookup"><span data-stu-id="9a601-130">**Type**</span></span>|<span data-ttu-id="9a601-131">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="9a601-131">**Required**</span></span>|<span data-ttu-id="9a601-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="9a601-132">**Description**</span></span>|<span data-ttu-id="9a601-133">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="9a601-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9a601-134">Del</span><span class="sxs-lookup"><span data-stu-id="9a601-134">Del</span></span>  <br/> |<span data-ttu-id="9a601-135">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9a601-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9a601-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a601-136">optional</span></span>  <br/> ||<span data-ttu-id="9a601-137">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9a601-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9a601-138">ID</span><span class="sxs-lookup"><span data-stu-id="9a601-138">ID</span></span>  <br/> |<span data-ttu-id="9a601-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a601-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a601-140">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9a601-140">required</span></span>  <br/> ||<span data-ttu-id="9a601-141">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a601-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a601-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="9a601-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="9a601-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9a601-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9a601-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a601-144">optional</span></span>  <br/> ||<span data-ttu-id="9a601-145">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9a601-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9a601-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="9a601-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="9a601-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9a601-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9a601-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a601-148">optional</span></span>  <br/> ||<span data-ttu-id="9a601-149">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9a601-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9a601-150">Master</span><span class="sxs-lookup"><span data-stu-id="9a601-150">Master</span></span>  <br/> |<span data-ttu-id="9a601-151">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a601-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a601-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a601-152">optional</span></span>  <br/> ||<span data-ttu-id="9a601-153">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a601-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a601-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="9a601-154">MasterShape</span></span>  <br/> |<span data-ttu-id="9a601-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a601-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a601-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a601-156">optional</span></span>  <br/> ||<span data-ttu-id="9a601-157">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a601-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a601-158">Nom</span><span class="sxs-lookup"><span data-stu-id="9a601-158">Name</span></span>  <br/> |<span data-ttu-id="9a601-159">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a601-159">xsd:string</span></span>  <br/> |<span data-ttu-id="9a601-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a601-160">optional</span></span>  <br/> ||<span data-ttu-id="9a601-161">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a601-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a601-162">NameU</span><span class="sxs-lookup"><span data-stu-id="9a601-162">NameU</span></span>  <br/> |<span data-ttu-id="9a601-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a601-163">xsd:string</span></span>  <br/> |<span data-ttu-id="9a601-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a601-164">optional</span></span>  <br/> ||<span data-ttu-id="9a601-165">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a601-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a601-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="9a601-166">OriginalID</span></span>  <br/> |<span data-ttu-id="9a601-167">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a601-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a601-168">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a601-168">optional</span></span>  <br/> ||<span data-ttu-id="9a601-169">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a601-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a601-170">Type</span><span class="sxs-lookup"><span data-stu-id="9a601-170">Type</span></span>  <br/> |<span data-ttu-id="9a601-171">xsd:token</span><span class="sxs-lookup"><span data-stu-id="9a601-171">xsd:token</span></span>  <br/> |<span data-ttu-id="9a601-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a601-172">optional</span></span>  <br/> ||<span data-ttu-id="9a601-173">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="9a601-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="9a601-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="9a601-174">UniqueID</span></span>  <br/> |<span data-ttu-id="9a601-175">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a601-175">xsd:string</span></span>  <br/> |<span data-ttu-id="9a601-176">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a601-176">optional</span></span>  <br/> ||<span data-ttu-id="9a601-177">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a601-177">Values of the xsd:string type.</span></span>  <br/> |
   

