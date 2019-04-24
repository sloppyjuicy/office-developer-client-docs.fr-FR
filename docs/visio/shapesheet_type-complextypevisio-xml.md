---
title: ComplexType ShapeSheet_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: c48af0def561e01fe5a92a57b7416faab40f1200
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349132"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="b2cb2-102">ComplexType ShapeSheet_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="b2cb2-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b2cb2-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="b2cb2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2cb2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b2cb2-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b2cb2-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="b2cb2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b2cb2-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b2cb2-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="b2cb2-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b2cb2-109">Définition</span><span class="sxs-lookup"><span data-stu-id="b2cb2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b2cb2-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="b2cb2-110">Elements and attributes</span></span>

<span data-ttu-id="b2cb2-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b2cb2-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b2cb2-112">Child elements</span></span>

|<span data-ttu-id="b2cb2-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-113">**Element**</span></span>|<span data-ttu-id="b2cb2-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-114">**Type**</span></span>|<span data-ttu-id="b2cb2-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b2cb2-116">Data1</span><span class="sxs-lookup"><span data-stu-id="b2cb2-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2cb2-117">Type_de_données</span><span class="sxs-lookup"><span data-stu-id="b2cb2-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b2cb2-118">Data2</span><span class="sxs-lookup"><span data-stu-id="b2cb2-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2cb2-119">Type_de_données</span><span class="sxs-lookup"><span data-stu-id="b2cb2-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b2cb2-120">Data3</span><span class="sxs-lookup"><span data-stu-id="b2cb2-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2cb2-121">Type_de_données</span><span class="sxs-lookup"><span data-stu-id="b2cb2-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b2cb2-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="b2cb2-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2cb2-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="b2cb2-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b2cb2-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="b2cb2-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2cb2-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="b2cb2-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b2cb2-126">Text</span><span class="sxs-lookup"><span data-stu-id="b2cb2-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2cb2-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="b2cb2-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b2cb2-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="b2cb2-128">Attributes</span></span>

|<span data-ttu-id="b2cb2-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-129">**Attribute**</span></span>|<span data-ttu-id="b2cb2-130">**Type**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-130">**Type**</span></span>|<span data-ttu-id="b2cb2-131">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-131">**Required**</span></span>|<span data-ttu-id="b2cb2-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-132">**Description**</span></span>|<span data-ttu-id="b2cb2-133">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2cb2-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b2cb2-134">Suppr</span><span class="sxs-lookup"><span data-stu-id="b2cb2-134">Del</span></span>  <br/> |<span data-ttu-id="b2cb2-135">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="b2cb2-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b2cb2-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="b2cb2-136">optional</span></span>  <br/> ||<span data-ttu-id="b2cb2-137">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b2cb2-138">ID</span><span class="sxs-lookup"><span data-stu-id="b2cb2-138">ID</span></span>  <br/> |<span data-ttu-id="b2cb2-139">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b2cb2-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b2cb2-140">obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2cb2-140">required</span></span>  <br/> ||<span data-ttu-id="b2cb2-141">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b2cb2-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="b2cb2-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="b2cb2-143">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="b2cb2-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b2cb2-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="b2cb2-144">optional</span></span>  <br/> ||<span data-ttu-id="b2cb2-145">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b2cb2-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="b2cb2-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="b2cb2-147">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="b2cb2-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b2cb2-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="b2cb2-148">optional</span></span>  <br/> ||<span data-ttu-id="b2cb2-149">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b2cb2-150">Master</span><span class="sxs-lookup"><span data-stu-id="b2cb2-150">Master</span></span>  <br/> |<span data-ttu-id="b2cb2-151">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b2cb2-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b2cb2-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="b2cb2-152">optional</span></span>  <br/> ||<span data-ttu-id="b2cb2-153">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b2cb2-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="b2cb2-154">MasterShape</span></span>  <br/> |<span data-ttu-id="b2cb2-155">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b2cb2-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b2cb2-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="b2cb2-156">optional</span></span>  <br/> ||<span data-ttu-id="b2cb2-157">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b2cb2-158">Nom</span><span class="sxs-lookup"><span data-stu-id="b2cb2-158">Name</span></span>  <br/> |<span data-ttu-id="b2cb2-159">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b2cb2-159">xsd:string</span></span>  <br/> |<span data-ttu-id="b2cb2-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="b2cb2-160">optional</span></span>  <br/> ||<span data-ttu-id="b2cb2-161">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b2cb2-162">NameU</span><span class="sxs-lookup"><span data-stu-id="b2cb2-162">NameU</span></span>  <br/> |<span data-ttu-id="b2cb2-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b2cb2-163">xsd:string</span></span>  <br/> |<span data-ttu-id="b2cb2-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="b2cb2-164">optional</span></span>  <br/> ||<span data-ttu-id="b2cb2-165">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b2cb2-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="b2cb2-166">OriginalID</span></span>  <br/> |<span data-ttu-id="b2cb2-167">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b2cb2-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b2cb2-168">facultatif</span><span class="sxs-lookup"><span data-stu-id="b2cb2-168">optional</span></span>  <br/> ||<span data-ttu-id="b2cb2-169">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b2cb2-170">Type</span><span class="sxs-lookup"><span data-stu-id="b2cb2-170">Type</span></span>  <br/> |<span data-ttu-id="b2cb2-171">xsd: Token</span><span class="sxs-lookup"><span data-stu-id="b2cb2-171">xsd:token</span></span>  <br/> |<span data-ttu-id="b2cb2-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="b2cb2-172">optional</span></span>  <br/> ||<span data-ttu-id="b2cb2-173">Valeurs du type xsd: Token.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="b2cb2-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="b2cb2-174">UniqueID</span></span>  <br/> |<span data-ttu-id="b2cb2-175">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b2cb2-175">xsd:string</span></span>  <br/> |<span data-ttu-id="b2cb2-176">facultatif</span><span class="sxs-lookup"><span data-stu-id="b2cb2-176">optional</span></span>  <br/> ||<span data-ttu-id="b2cb2-177">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b2cb2-177">Values of the xsd:string type.</span></span>  <br/> |
   

