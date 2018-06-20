---
title: Type complexe ShapeSheet_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: 45282acfc8a399a5c634c1860aba1f926e0b7a94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789671"
---
# <a name="shapesheettype-complextype-visio-xml"></a><span data-ttu-id="ff5fa-102">Type complexe ShapeSheet_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="ff5fa-102">ShapeSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ff5fa-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="ff5fa-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff5fa-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="ff5fa-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ff5fa-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ff5fa-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ff5fa-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ff5fa-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ff5fa-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="ff5fa-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ff5fa-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="ff5fa-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ff5fa-109">Définition</span><span class="sxs-lookup"><span data-stu-id="ff5fa-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ff5fa-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ff5fa-110">Elements and attributes</span></span>

<span data-ttu-id="ff5fa-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ff5fa-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ff5fa-112">Child elements</span></span>

|<span data-ttu-id="ff5fa-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ff5fa-113">**Element**</span></span>|<span data-ttu-id="ff5fa-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="ff5fa-114">**Type**</span></span>|<span data-ttu-id="ff5fa-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="ff5fa-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ff5fa-116">Data1</span><span class="sxs-lookup"><span data-stu-id="ff5fa-116">Data1</span></span>](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ff5fa-117">Type_de_données</span><span class="sxs-lookup"><span data-stu-id="ff5fa-117">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ff5fa-118">Data2</span><span class="sxs-lookup"><span data-stu-id="ff5fa-118">Data2</span></span>](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ff5fa-119">Type_de_données</span><span class="sxs-lookup"><span data-stu-id="ff5fa-119">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ff5fa-120">Data3</span><span class="sxs-lookup"><span data-stu-id="ff5fa-120">Data3</span></span>](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ff5fa-121">Type_de_données</span><span class="sxs-lookup"><span data-stu-id="ff5fa-121">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ff5fa-122">ForeignData</span><span class="sxs-lookup"><span data-stu-id="ff5fa-122">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ff5fa-123">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="ff5fa-123">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ff5fa-124">Shapes</span><span class="sxs-lookup"><span data-stu-id="ff5fa-124">Shapes</span></span>](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ff5fa-125">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="ff5fa-125">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ff5fa-126">Text</span><span class="sxs-lookup"><span data-stu-id="ff5fa-126">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ff5fa-127">Text_Type</span><span class="sxs-lookup"><span data-stu-id="ff5fa-127">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ff5fa-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="ff5fa-128">Attributes</span></span>

|<span data-ttu-id="ff5fa-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ff5fa-129">**Attribute**</span></span>|<span data-ttu-id="ff5fa-130">**Type**</span><span class="sxs-lookup"><span data-stu-id="ff5fa-130">**Type**</span></span>|<span data-ttu-id="ff5fa-131">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ff5fa-131">**Required**</span></span>|<span data-ttu-id="ff5fa-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="ff5fa-132">**Description**</span></span>|<span data-ttu-id="ff5fa-133">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ff5fa-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ff5fa-134">SUPPR.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-134">Del</span></span>  <br/> |<span data-ttu-id="ff5fa-135">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="ff5fa-135">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ff5fa-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff5fa-136">optional</span></span>  <br/> ||<span data-ttu-id="ff5fa-137">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-137">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ff5fa-138">ID</span><span class="sxs-lookup"><span data-stu-id="ff5fa-138">ID</span></span>  <br/> |<span data-ttu-id="ff5fa-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff5fa-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff5fa-140">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ff5fa-140">required</span></span>  <br/> ||<span data-ttu-id="ff5fa-141">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff5fa-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="ff5fa-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="ff5fa-143">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="ff5fa-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ff5fa-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff5fa-144">optional</span></span>  <br/> ||<span data-ttu-id="ff5fa-145">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ff5fa-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="ff5fa-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="ff5fa-147">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="ff5fa-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ff5fa-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff5fa-148">optional</span></span>  <br/> ||<span data-ttu-id="ff5fa-149">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ff5fa-150">Master</span><span class="sxs-lookup"><span data-stu-id="ff5fa-150">Master</span></span>  <br/> |<span data-ttu-id="ff5fa-151">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff5fa-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff5fa-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff5fa-152">optional</span></span>  <br/> ||<span data-ttu-id="ff5fa-153">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff5fa-154">MasterShape</span><span class="sxs-lookup"><span data-stu-id="ff5fa-154">MasterShape</span></span>  <br/> |<span data-ttu-id="ff5fa-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff5fa-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff5fa-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff5fa-156">optional</span></span>  <br/> ||<span data-ttu-id="ff5fa-157">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff5fa-158">Nom</span><span class="sxs-lookup"><span data-stu-id="ff5fa-158">Name</span></span>  <br/> |<span data-ttu-id="ff5fa-159">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ff5fa-159">xsd:string</span></span>  <br/> |<span data-ttu-id="ff5fa-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff5fa-160">optional</span></span>  <br/> ||<span data-ttu-id="ff5fa-161">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff5fa-162">NameU</span><span class="sxs-lookup"><span data-stu-id="ff5fa-162">NameU</span></span>  <br/> |<span data-ttu-id="ff5fa-163">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ff5fa-163">xsd:string</span></span>  <br/> |<span data-ttu-id="ff5fa-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff5fa-164">optional</span></span>  <br/> ||<span data-ttu-id="ff5fa-165">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-165">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ff5fa-166">OriginalID</span><span class="sxs-lookup"><span data-stu-id="ff5fa-166">OriginalID</span></span>  <br/> |<span data-ttu-id="ff5fa-167">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff5fa-167">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff5fa-168">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff5fa-168">optional</span></span>  <br/> ||<span data-ttu-id="ff5fa-169">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-169">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff5fa-170">Type</span><span class="sxs-lookup"><span data-stu-id="ff5fa-170">Type</span></span>  <br/> |<span data-ttu-id="ff5fa-171">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="ff5fa-171">xsd:token</span></span>  <br/> |<span data-ttu-id="ff5fa-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff5fa-172">optional</span></span>  <br/> ||<span data-ttu-id="ff5fa-173">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-173">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="ff5fa-174">UniqueID</span><span class="sxs-lookup"><span data-stu-id="ff5fa-174">UniqueID</span></span>  <br/> |<span data-ttu-id="ff5fa-175">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ff5fa-175">xsd:string</span></span>  <br/> |<span data-ttu-id="ff5fa-176">facultatif</span><span class="sxs-lookup"><span data-stu-id="ff5fa-176">optional</span></span>  <br/> ||<span data-ttu-id="ff5fa-177">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ff5fa-177">Values of the xsd:string type.</span></span>  <br/> |
   

