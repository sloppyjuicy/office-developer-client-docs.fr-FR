---
title: ComplexType Window_Type (Visio XML)
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
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="a065e-102">ComplexType Window_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a065e-102">Window_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a065e-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a065e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a065e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a065e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a065e-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a065e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a065e-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="a065e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a065e-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a065e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a065e-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="a065e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a065e-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a065e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a065e-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a065e-110">Elements and attributes</span></span>

<span data-ttu-id="a065e-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="a065e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a065e-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a065e-112">Child elements</span></span>

|<span data-ttu-id="a065e-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a065e-113">**Element**</span></span>|<span data-ttu-id="a065e-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="a065e-114">**Type**</span></span>|<span data-ttu-id="a065e-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a065e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a065e-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="a065e-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="a065e-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="a065e-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="a065e-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="a065e-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="a065e-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="a065e-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="a065e-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="a065e-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="a065e-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="a065e-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="a065e-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a065e-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="a065e-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a065e-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="a065e-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a065e-142">Attributs</span><span class="sxs-lookup"><span data-stu-id="a065e-142">Attributes</span></span>

|<span data-ttu-id="a065e-143">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a065e-143">**Attribute**</span></span>|<span data-ttu-id="a065e-144">**Type**</span><span class="sxs-lookup"><span data-stu-id="a065e-144">**Type**</span></span>|<span data-ttu-id="a065e-145">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a065e-145">**Required**</span></span>|<span data-ttu-id="a065e-146">**Description**</span><span class="sxs-lookup"><span data-stu-id="a065e-146">**Description**</span></span>|<span data-ttu-id="a065e-147">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a065e-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a065e-148">Container</span><span class="sxs-lookup"><span data-stu-id="a065e-148">Container</span></span>  <br/> |<span data-ttu-id="a065e-149">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a065e-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a065e-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-150">optional</span></span>  <br/> ||<span data-ttu-id="a065e-151">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a065e-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a065e-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="a065e-152">ContainerType</span></span>  <br/> |<span data-ttu-id="a065e-153">xsd: Token</span><span class="sxs-lookup"><span data-stu-id="a065e-153">xsd:token</span></span>  <br/> |<span data-ttu-id="a065e-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-154">optional</span></span>  <br/> ||<span data-ttu-id="a065e-155">Valeurs du type xsd: Token.</span><span class="sxs-lookup"><span data-stu-id="a065e-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a065e-156">Document</span><span class="sxs-lookup"><span data-stu-id="a065e-156">Document</span></span>  <br/> |<span data-ttu-id="a065e-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="a065e-157">xsd:string</span></span>  <br/> |<span data-ttu-id="a065e-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-158">optional</span></span>  <br/> ||<span data-ttu-id="a065e-159">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="a065e-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a065e-160">ID</span><span class="sxs-lookup"><span data-stu-id="a065e-160">ID</span></span>  <br/> |<span data-ttu-id="a065e-161">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a065e-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a065e-162">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a065e-162">required</span></span>  <br/> ||<span data-ttu-id="a065e-163">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a065e-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a065e-164">Master</span><span class="sxs-lookup"><span data-stu-id="a065e-164">Master</span></span>  <br/> |<span data-ttu-id="a065e-165">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a065e-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a065e-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-166">optional</span></span>  <br/> ||<span data-ttu-id="a065e-167">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a065e-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a065e-168">Page</span><span class="sxs-lookup"><span data-stu-id="a065e-168">Page</span></span>  <br/> |<span data-ttu-id="a065e-169">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a065e-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a065e-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-170">optional</span></span>  <br/> ||<span data-ttu-id="a065e-171">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a065e-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a065e-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="a065e-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="a065e-173">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a065e-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a065e-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-174">optional</span></span>  <br/> ||<span data-ttu-id="a065e-175">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a065e-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a065e-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a065e-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="a065e-177">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="a065e-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a065e-178">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-178">optional</span></span>  <br/> ||<span data-ttu-id="a065e-179">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="a065e-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a065e-180">Sheet</span><span class="sxs-lookup"><span data-stu-id="a065e-180">Sheet</span></span>  <br/> |<span data-ttu-id="a065e-181">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a065e-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a065e-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-182">optional</span></span>  <br/> ||<span data-ttu-id="a065e-183">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a065e-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a065e-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="a065e-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="a065e-185">xsd: double</span><span class="sxs-lookup"><span data-stu-id="a065e-185">xsd:double</span></span>  <br/> |<span data-ttu-id="a065e-186">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-186">optional</span></span>  <br/> ||<span data-ttu-id="a065e-187">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="a065e-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a065e-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="a065e-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="a065e-189">xsd: double</span><span class="sxs-lookup"><span data-stu-id="a065e-189">xsd:double</span></span>  <br/> |<span data-ttu-id="a065e-190">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-190">optional</span></span>  <br/> ||<span data-ttu-id="a065e-191">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="a065e-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a065e-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="a065e-192">ViewScale</span></span>  <br/> |<span data-ttu-id="a065e-193">xsd: double</span><span class="sxs-lookup"><span data-stu-id="a065e-193">xsd:double</span></span>  <br/> |<span data-ttu-id="a065e-194">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-194">optional</span></span>  <br/> ||<span data-ttu-id="a065e-195">Valeurs du type xsd: double.</span><span class="sxs-lookup"><span data-stu-id="a065e-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a065e-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="a065e-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="a065e-197">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a065e-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a065e-198">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-198">optional</span></span>  <br/> ||<span data-ttu-id="a065e-199">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a065e-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a065e-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="a065e-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="a065e-201">xsd: Short</span><span class="sxs-lookup"><span data-stu-id="a065e-201">xsd:short</span></span>  <br/> |<span data-ttu-id="a065e-202">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-202">optional</span></span>  <br/> ||<span data-ttu-id="a065e-203">Valeurs du type xsd: short.</span><span class="sxs-lookup"><span data-stu-id="a065e-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="a065e-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="a065e-204">WindowState</span></span>  <br/> |<span data-ttu-id="a065e-205">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a065e-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a065e-206">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-206">optional</span></span>  <br/> ||<span data-ttu-id="a065e-207">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a065e-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a065e-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="a065e-208">WindowTop</span></span>  <br/> |<span data-ttu-id="a065e-209">xsd: Short</span><span class="sxs-lookup"><span data-stu-id="a065e-209">xsd:short</span></span>  <br/> |<span data-ttu-id="a065e-210">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-210">optional</span></span>  <br/> ||<span data-ttu-id="a065e-211">Valeurs du type xsd: short.</span><span class="sxs-lookup"><span data-stu-id="a065e-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="a065e-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="a065e-212">WindowType</span></span>  <br/> |<span data-ttu-id="a065e-213">xsd: Token</span><span class="sxs-lookup"><span data-stu-id="a065e-213">xsd:token</span></span>  <br/> |<span data-ttu-id="a065e-214">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a065e-214">required</span></span>  <br/> ||<span data-ttu-id="a065e-215">Valeurs du type xsd: Token.</span><span class="sxs-lookup"><span data-stu-id="a065e-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a065e-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="a065e-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="a065e-217">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a065e-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a065e-218">facultatif</span><span class="sxs-lookup"><span data-stu-id="a065e-218">optional</span></span>  <br/> ||<span data-ttu-id="a065e-219">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a065e-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

