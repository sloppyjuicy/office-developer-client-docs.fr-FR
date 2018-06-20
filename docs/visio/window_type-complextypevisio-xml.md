---
title: Type complexe Window_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: dc4dda48c037f7af03ee22a07bee288ce5d30872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790039"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="a86d8-102">Type complexe Window_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="a86d8-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a86d8-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="a86d8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a86d8-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="a86d8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a86d8-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a86d8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a86d8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a86d8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a86d8-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="a86d8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a86d8-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="a86d8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a86d8-109">Définition</span><span class="sxs-lookup"><span data-stu-id="a86d8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a86d8-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a86d8-110">Elements and attributes</span></span>

<span data-ttu-id="a86d8-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="a86d8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a86d8-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a86d8-112">Child elements</span></span>

|<span data-ttu-id="a86d8-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a86d8-113">**Element**</span></span>|<span data-ttu-id="a86d8-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="a86d8-114">**Type**</span></span>|<span data-ttu-id="a86d8-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a86d8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a86d8-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="a86d8-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="a86d8-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="a86d8-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="a86d8-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="a86d8-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="a86d8-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="a86d8-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="a86d8-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="a86d8-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="a86d8-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="a86d8-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="a86d8-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a86d8-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="a86d8-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a86d8-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="a86d8-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a86d8-142">Attributs</span><span class="sxs-lookup"><span data-stu-id="a86d8-142">Attributes</span></span>

|<span data-ttu-id="a86d8-143">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a86d8-143">**Attribute**</span></span>|<span data-ttu-id="a86d8-144">**Type**</span><span class="sxs-lookup"><span data-stu-id="a86d8-144">**Type**</span></span>|<span data-ttu-id="a86d8-145">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="a86d8-145">**Required**</span></span>|<span data-ttu-id="a86d8-146">**Description**</span><span class="sxs-lookup"><span data-stu-id="a86d8-146">**Description**</span></span>|<span data-ttu-id="a86d8-147">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="a86d8-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a86d8-148">Container</span><span class="sxs-lookup"><span data-stu-id="a86d8-148">Container</span></span>  <br/> |<span data-ttu-id="a86d8-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a86d8-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a86d8-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-150">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-151">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a86d8-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="a86d8-152">ContainerType</span></span>  <br/> |<span data-ttu-id="a86d8-153">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="a86d8-153">xsd:token</span></span>  <br/> |<span data-ttu-id="a86d8-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-154">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-155">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="a86d8-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-156">Document</span><span class="sxs-lookup"><span data-stu-id="a86d8-156">Document</span></span>  <br/> |<span data-ttu-id="a86d8-157">XSD : String</span><span class="sxs-lookup"><span data-stu-id="a86d8-157">xsd:string</span></span>  <br/> |<span data-ttu-id="a86d8-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-158">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-159">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="a86d8-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-160">ID</span><span class="sxs-lookup"><span data-stu-id="a86d8-160">ID</span></span>  <br/> |<span data-ttu-id="a86d8-161">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a86d8-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a86d8-162">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a86d8-162">required</span></span>  <br/> ||<span data-ttu-id="a86d8-163">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a86d8-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-164">Master</span><span class="sxs-lookup"><span data-stu-id="a86d8-164">Master</span></span>  <br/> |<span data-ttu-id="a86d8-165">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a86d8-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a86d8-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-166">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-167">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a86d8-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-168">Page</span><span class="sxs-lookup"><span data-stu-id="a86d8-168">Page</span></span>  <br/> |<span data-ttu-id="a86d8-169">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a86d8-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a86d8-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-170">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-171">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a86d8-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="a86d8-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="a86d8-173">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a86d8-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a86d8-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-174">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-175">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a86d8-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a86d8-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="a86d8-177">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="a86d8-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a86d8-178">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-178">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-179">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="a86d8-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-180">Feuille</span><span class="sxs-lookup"><span data-stu-id="a86d8-180">Sheet</span></span>  <br/> |<span data-ttu-id="a86d8-181">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a86d8-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a86d8-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-182">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-183">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a86d8-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="a86d8-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="a86d8-185">XSD : double</span><span class="sxs-lookup"><span data-stu-id="a86d8-185">xsd:double</span></span>  <br/> |<span data-ttu-id="a86d8-186">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-186">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-187">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="a86d8-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="a86d8-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="a86d8-189">XSD : double</span><span class="sxs-lookup"><span data-stu-id="a86d8-189">xsd:double</span></span>  <br/> |<span data-ttu-id="a86d8-190">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-190">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-191">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="a86d8-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="a86d8-192">ViewScale</span></span>  <br/> |<span data-ttu-id="a86d8-193">XSD : double</span><span class="sxs-lookup"><span data-stu-id="a86d8-193">xsd:double</span></span>  <br/> |<span data-ttu-id="a86d8-194">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-194">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-195">Valeurs du type xsd : double.</span><span class="sxs-lookup"><span data-stu-id="a86d8-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-196">WindowHeight (HauteurFenêtre)</span><span class="sxs-lookup"><span data-stu-id="a86d8-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="a86d8-197">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a86d8-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a86d8-198">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-198">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-199">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a86d8-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="a86d8-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="a86d8-201">XSD:short</span><span class="sxs-lookup"><span data-stu-id="a86d8-201">xsd:short</span></span>  <br/> |<span data-ttu-id="a86d8-202">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-202">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-203">Valeurs du type xsd:short.</span><span class="sxs-lookup"><span data-stu-id="a86d8-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="a86d8-204">WindowState</span></span>  <br/> |<span data-ttu-id="a86d8-205">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a86d8-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a86d8-206">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-206">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-207">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a86d8-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="a86d8-208">WindowTop</span></span>  <br/> |<span data-ttu-id="a86d8-209">XSD:short</span><span class="sxs-lookup"><span data-stu-id="a86d8-209">xsd:short</span></span>  <br/> |<span data-ttu-id="a86d8-210">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-210">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-211">Valeurs du type xsd:short.</span><span class="sxs-lookup"><span data-stu-id="a86d8-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-212">Propriété WindowType</span><span class="sxs-lookup"><span data-stu-id="a86d8-212">WindowType</span></span>  <br/> |<span data-ttu-id="a86d8-213">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="a86d8-213">xsd:token</span></span>  <br/> |<span data-ttu-id="a86d8-214">obligatoire</span><span class="sxs-lookup"><span data-stu-id="a86d8-214">required</span></span>  <br/> ||<span data-ttu-id="a86d8-215">Valeurs du type xsd:token.</span><span class="sxs-lookup"><span data-stu-id="a86d8-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="a86d8-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="a86d8-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="a86d8-217">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a86d8-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a86d8-218">facultatif</span><span class="sxs-lookup"><span data-stu-id="a86d8-218">optional</span></span>  <br/> ||<span data-ttu-id="a86d8-219">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a86d8-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

