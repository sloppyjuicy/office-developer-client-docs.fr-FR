---
title: Window_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 08b65a5f0e108c5503e29c7e195d681d0a343521
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538451"
---
# <a name="window_type-complextype-visio-xml"></a><span data-ttu-id="7a17a-102">Window_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7a17a-102">Window_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="7a17a-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7a17a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a17a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7a17a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7a17a-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7a17a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7a17a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7a17a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7a17a-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7a17a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7a17a-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="7a17a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7a17a-109">Définition</span><span class="sxs-lookup"><span data-stu-id="7a17a-109">Definition</span></span>

```XML
          <xs:complexType name="Window_Type">
          
          <xs:sequence>
    <xs:element name="StencilGroup"  type="StencilGroup_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StencilGroupPos"  type="StencilGroupPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowRulers"  type="ShowRulers_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGrid"  type="ShowGrid_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowPageBreaks"  type="ShowPageBreaks_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGuides"  type="ShowGuides_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowConnectionPoints"  type="ShowConnectionPoints_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="GlueSettings"  type="GlueSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapSettings"  type="SnapSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapExtensions"  type="SnapExtensions_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapAngles"  type="SnapAngles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DynamicGridEnabled"  type="DynamicGridEnabled_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="TabSplitterPos"  type="TabSplitterPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="WindowType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="WindowState"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Document"
  type="xsd:string"
    />
    <xs:attribute name="WindowLeft"
  type="xsd:short"
    />
    <xs:attribute name="WindowTop"
  type="xsd:short"
    />
    <xs:attribute name="WindowWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="WindowHeight"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ContainerType"
  type="xsd:token"
    />
    <xs:attribute name="Container"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Sheet"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReadOnly"
  type="xsd:boolean"
    />
    <xs:attribute name="ParentWindow"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Page"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7a17a-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7a17a-110">Elements and attributes</span></span>

<span data-ttu-id="7a17a-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="7a17a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7a17a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7a17a-112">Child elements</span></span>

|<span data-ttu-id="7a17a-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7a17a-113">**Element**</span></span>|<span data-ttu-id="7a17a-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="7a17a-114">**Type**</span></span>|<span data-ttu-id="7a17a-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="7a17a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7a17a-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="7a17a-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="7a17a-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="7a17a-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="7a17a-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="7a17a-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="7a17a-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="7a17a-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="7a17a-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="7a17a-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="7a17a-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="7a17a-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="7a17a-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7a17a-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="7a17a-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7a17a-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="7a17a-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7a17a-142">Attributs</span><span class="sxs-lookup"><span data-stu-id="7a17a-142">Attributes</span></span>

|<span data-ttu-id="7a17a-143">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7a17a-143">**Attribute**</span></span>|<span data-ttu-id="7a17a-144">**Type**</span><span class="sxs-lookup"><span data-stu-id="7a17a-144">**Type**</span></span>|<span data-ttu-id="7a17a-145">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="7a17a-145">**Required**</span></span>|<span data-ttu-id="7a17a-146">**Description**</span><span class="sxs-lookup"><span data-stu-id="7a17a-146">**Description**</span></span>|<span data-ttu-id="7a17a-147">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="7a17a-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7a17a-148">Container</span><span class="sxs-lookup"><span data-stu-id="7a17a-148">Container</span></span>  <br/> |<span data-ttu-id="7a17a-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7a17a-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7a17a-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-150">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-151">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7a17a-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="7a17a-152">ContainerType</span></span>  <br/> |<span data-ttu-id="7a17a-153">xsd:token</span><span class="sxs-lookup"><span data-stu-id="7a17a-153">xsd:token</span></span>  <br/> |<span data-ttu-id="7a17a-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-154">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-155">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="7a17a-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-156">Document</span><span class="sxs-lookup"><span data-stu-id="7a17a-156">Document</span></span>  <br/> |<span data-ttu-id="7a17a-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7a17a-157">xsd:string</span></span>  <br/> |<span data-ttu-id="7a17a-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-158">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-159">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7a17a-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-160">ID</span><span class="sxs-lookup"><span data-stu-id="7a17a-160">ID</span></span>  <br/> |<span data-ttu-id="7a17a-161">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7a17a-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7a17a-162">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7a17a-162">required</span></span>  <br/> ||<span data-ttu-id="7a17a-163">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7a17a-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-164">Master</span><span class="sxs-lookup"><span data-stu-id="7a17a-164">Master</span></span>  <br/> |<span data-ttu-id="7a17a-165">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7a17a-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7a17a-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-166">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-167">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7a17a-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-168">Page</span><span class="sxs-lookup"><span data-stu-id="7a17a-168">Page</span></span>  <br/> |<span data-ttu-id="7a17a-169">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7a17a-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7a17a-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-170">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-171">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7a17a-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="7a17a-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="7a17a-173">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7a17a-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7a17a-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-174">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-175">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7a17a-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="7a17a-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="7a17a-177">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="7a17a-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7a17a-178">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-178">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-179">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="7a17a-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-180">Sheet</span><span class="sxs-lookup"><span data-stu-id="7a17a-180">Sheet</span></span>  <br/> |<span data-ttu-id="7a17a-181">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7a17a-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7a17a-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-182">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-183">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7a17a-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="7a17a-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="7a17a-185">xsd:double</span><span class="sxs-lookup"><span data-stu-id="7a17a-185">xsd:double</span></span>  <br/> |<span data-ttu-id="7a17a-186">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-186">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-187">Valeurs du type xsd:double.</span><span class="sxs-lookup"><span data-stu-id="7a17a-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="7a17a-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="7a17a-189">xsd:double</span><span class="sxs-lookup"><span data-stu-id="7a17a-189">xsd:double</span></span>  <br/> |<span data-ttu-id="7a17a-190">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-190">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-191">Valeurs du type xsd:double.</span><span class="sxs-lookup"><span data-stu-id="7a17a-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="7a17a-192">ViewScale</span></span>  <br/> |<span data-ttu-id="7a17a-193">xsd:double</span><span class="sxs-lookup"><span data-stu-id="7a17a-193">xsd:double</span></span>  <br/> |<span data-ttu-id="7a17a-194">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-194">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-195">Valeurs du type xsd:double.</span><span class="sxs-lookup"><span data-stu-id="7a17a-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="7a17a-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="7a17a-197">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7a17a-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7a17a-198">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-198">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-199">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7a17a-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="7a17a-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="7a17a-201">xsd:short</span><span class="sxs-lookup"><span data-stu-id="7a17a-201">xsd:short</span></span>  <br/> |<span data-ttu-id="7a17a-202">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-202">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-203">Valeurs du type xsd:short.</span><span class="sxs-lookup"><span data-stu-id="7a17a-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="7a17a-204">WindowState</span></span>  <br/> |<span data-ttu-id="7a17a-205">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7a17a-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7a17a-206">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-206">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-207">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7a17a-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="7a17a-208">WindowTop</span></span>  <br/> |<span data-ttu-id="7a17a-209">xsd:short</span><span class="sxs-lookup"><span data-stu-id="7a17a-209">xsd:short</span></span>  <br/> |<span data-ttu-id="7a17a-210">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-210">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-211">Valeurs du type xsd:short.</span><span class="sxs-lookup"><span data-stu-id="7a17a-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="7a17a-212">WindowType</span></span>  <br/> |<span data-ttu-id="7a17a-213">xsd:token</span><span class="sxs-lookup"><span data-stu-id="7a17a-213">xsd:token</span></span>  <br/> |<span data-ttu-id="7a17a-214">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7a17a-214">required</span></span>  <br/> ||<span data-ttu-id="7a17a-215">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="7a17a-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="7a17a-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="7a17a-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="7a17a-217">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7a17a-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7a17a-218">facultatif</span><span class="sxs-lookup"><span data-stu-id="7a17a-218">optional</span></span>  <br/> ||<span data-ttu-id="7a17a-219">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7a17a-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

