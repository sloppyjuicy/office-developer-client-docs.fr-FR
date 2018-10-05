---
title: Type complexe Window_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 340326213de4029201d21e627ed4b27c53b33d1e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400585"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="125f1-102">Type complexe Window_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="125f1-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="125f1-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="125f1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="125f1-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="125f1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="125f1-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="125f1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="125f1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="125f1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="125f1-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="125f1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="125f1-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="125f1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="125f1-109">Définition</span><span class="sxs-lookup"><span data-stu-id="125f1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="125f1-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="125f1-110">Elements and attributes</span></span>

<span data-ttu-id="125f1-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="125f1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="125f1-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="125f1-112">Child elements</span></span>

|<span data-ttu-id="125f1-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="125f1-113">**Element**</span></span>|<span data-ttu-id="125f1-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="125f1-114">**Type**</span></span>|<span data-ttu-id="125f1-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="125f1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="125f1-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="125f1-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="125f1-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="125f1-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="125f1-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="125f1-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="125f1-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="125f1-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="125f1-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="125f1-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="125f1-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="125f1-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="125f1-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="125f1-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="125f1-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="125f1-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="125f1-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="125f1-142">Attributs</span><span class="sxs-lookup"><span data-stu-id="125f1-142">Attributes</span></span>

|<span data-ttu-id="125f1-143">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="125f1-143">**Attribute**</span></span>|<span data-ttu-id="125f1-144">**Type**</span><span class="sxs-lookup"><span data-stu-id="125f1-144">**Type**</span></span>|<span data-ttu-id="125f1-145">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="125f1-145">**Required**</span></span>|<span data-ttu-id="125f1-146">**Description**</span><span class="sxs-lookup"><span data-stu-id="125f1-146">**Description**</span></span>|<span data-ttu-id="125f1-147">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="125f1-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="125f1-148">Container</span><span class="sxs-lookup"><span data-stu-id="125f1-148">Container</span></span>  <br/> |<span data-ttu-id="125f1-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="125f1-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="125f1-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-150">optional</span></span>  <br/> ||<span data-ttu-id="125f1-151">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="125f1-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="125f1-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="125f1-152">ContainerType</span></span>  <br/> |<span data-ttu-id="125f1-153">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="125f1-153">xsd:token</span></span>  <br/> |<span data-ttu-id="125f1-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-154">optional</span></span>  <br/> ||<span data-ttu-id="125f1-155">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="125f1-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="125f1-156">Document</span><span class="sxs-lookup"><span data-stu-id="125f1-156">Document</span></span>  <br/> |<span data-ttu-id="125f1-157">XSD : String</span><span class="sxs-lookup"><span data-stu-id="125f1-157">xsd:string</span></span>  <br/> |<span data-ttu-id="125f1-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-158">optional</span></span>  <br/> ||<span data-ttu-id="125f1-159">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="125f1-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="125f1-160">ID</span><span class="sxs-lookup"><span data-stu-id="125f1-160">ID</span></span>  <br/> |<span data-ttu-id="125f1-161">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="125f1-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="125f1-162">obligatoire</span><span class="sxs-lookup"><span data-stu-id="125f1-162">required</span></span>  <br/> ||<span data-ttu-id="125f1-163">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="125f1-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="125f1-164">Master</span><span class="sxs-lookup"><span data-stu-id="125f1-164">Master</span></span>  <br/> |<span data-ttu-id="125f1-165">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="125f1-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="125f1-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-166">optional</span></span>  <br/> ||<span data-ttu-id="125f1-167">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="125f1-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="125f1-168">Page</span><span class="sxs-lookup"><span data-stu-id="125f1-168">Page</span></span>  <br/> |<span data-ttu-id="125f1-169">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="125f1-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="125f1-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-170">optional</span></span>  <br/> ||<span data-ttu-id="125f1-171">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="125f1-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="125f1-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="125f1-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="125f1-173">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="125f1-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="125f1-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-174">optional</span></span>  <br/> ||<span data-ttu-id="125f1-175">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="125f1-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="125f1-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="125f1-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="125f1-177">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="125f1-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="125f1-178">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-178">optional</span></span>  <br/> ||<span data-ttu-id="125f1-179">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="125f1-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="125f1-180">Feuille</span><span class="sxs-lookup"><span data-stu-id="125f1-180">Sheet</span></span>  <br/> |<span data-ttu-id="125f1-181">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="125f1-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="125f1-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-182">optional</span></span>  <br/> ||<span data-ttu-id="125f1-183">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="125f1-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="125f1-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="125f1-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="125f1-185">XSD : double</span><span class="sxs-lookup"><span data-stu-id="125f1-185">xsd:double</span></span>  <br/> |<span data-ttu-id="125f1-186">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-186">optional</span></span>  <br/> ||<span data-ttu-id="125f1-187">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="125f1-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="125f1-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="125f1-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="125f1-189">XSD : double</span><span class="sxs-lookup"><span data-stu-id="125f1-189">xsd:double</span></span>  <br/> |<span data-ttu-id="125f1-190">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-190">optional</span></span>  <br/> ||<span data-ttu-id="125f1-191">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="125f1-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="125f1-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="125f1-192">ViewScale</span></span>  <br/> |<span data-ttu-id="125f1-193">XSD : double</span><span class="sxs-lookup"><span data-stu-id="125f1-193">xsd:double</span></span>  <br/> |<span data-ttu-id="125f1-194">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-194">optional</span></span>  <br/> ||<span data-ttu-id="125f1-195">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="125f1-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="125f1-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="125f1-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="125f1-197">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="125f1-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="125f1-198">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-198">optional</span></span>  <br/> ||<span data-ttu-id="125f1-199">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="125f1-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="125f1-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="125f1-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="125f1-201">XSD:short</span><span class="sxs-lookup"><span data-stu-id="125f1-201">xsd:short</span></span>  <br/> |<span data-ttu-id="125f1-202">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-202">optional</span></span>  <br/> ||<span data-ttu-id="125f1-203">Valeurs du type xsd:short.</span><span class="sxs-lookup"><span data-stu-id="125f1-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="125f1-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="125f1-204">WindowState</span></span>  <br/> |<span data-ttu-id="125f1-205">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="125f1-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="125f1-206">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-206">optional</span></span>  <br/> ||<span data-ttu-id="125f1-207">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="125f1-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="125f1-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="125f1-208">WindowTop</span></span>  <br/> |<span data-ttu-id="125f1-209">XSD:short</span><span class="sxs-lookup"><span data-stu-id="125f1-209">xsd:short</span></span>  <br/> |<span data-ttu-id="125f1-210">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-210">optional</span></span>  <br/> ||<span data-ttu-id="125f1-211">Valeurs du type xsd:short.</span><span class="sxs-lookup"><span data-stu-id="125f1-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="125f1-212">Propriété WindowType</span><span class="sxs-lookup"><span data-stu-id="125f1-212">WindowType</span></span>  <br/> |<span data-ttu-id="125f1-213">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="125f1-213">xsd:token</span></span>  <br/> |<span data-ttu-id="125f1-214">obligatoire</span><span class="sxs-lookup"><span data-stu-id="125f1-214">required</span></span>  <br/> ||<span data-ttu-id="125f1-215">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="125f1-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="125f1-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="125f1-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="125f1-217">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="125f1-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="125f1-218">facultatif</span><span class="sxs-lookup"><span data-stu-id="125f1-218">optional</span></span>  <br/> ||<span data-ttu-id="125f1-219">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="125f1-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

