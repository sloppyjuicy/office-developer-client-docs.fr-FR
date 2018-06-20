---
title: Type complexe DocumentSettings_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 93623133e7d7fd096e063f0d9d5227d65dcc4736
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788522"
---
# <a name="documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="9a4d3-102">Type complexe DocumentSettings_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="9a4d3-102">DocumentSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9a4d3-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a4d3-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="9a4d3-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9a4d3-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9a4d3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9a4d3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9a4d3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9a4d3-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9a4d3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9a4d3-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="9a4d3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a4d3-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9a4d3-109">Definition</span></span>

```XML
          <xs:complexType name="DocumentSettings_Type">
          
          <xs:all>
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
    
    <xs:element name="ProtectStyles"  type="ProtectStyles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectShapes"  type="ProtectShapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectMasters"  type="ProtectMasters_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectBkgnds"  type="ProtectBkgnds_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomMenusFile"  type="CustomMenusFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomToolbarsFile"  type="CustomToolbarsFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="AttachedToolbars"  type="AttachedToolbars_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="TopPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultTextStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultLineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultFillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultGuideStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9a4d3-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9a4d3-110">Elements and attributes</span></span>

<span data-ttu-id="9a4d3-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="9a4d3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9a4d3-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9a4d3-112">Child elements</span></span>

|<span data-ttu-id="9a4d3-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="9a4d3-113">**Element**</span></span>|<span data-ttu-id="9a4d3-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="9a4d3-114">**Type**</span></span>|<span data-ttu-id="9a4d3-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="9a4d3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9a4d3-116">AttachedToolbars</span><span class="sxs-lookup"><span data-stu-id="9a4d3-116">AttachedToolbars</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-117">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-117">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a4d3-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="9a4d3-118">CustomMenusFile</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-119">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-119">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a4d3-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="9a4d3-120">CustomToolbarsFile</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-121">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-121">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a4d3-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="9a4d3-122">DynamicGridEnabled</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-123">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-123">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a4d3-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="9a4d3-124">GlueSettings</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-125">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-125">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a4d3-126">ProtectBkgnds</span><span class="sxs-lookup"><span data-stu-id="9a4d3-126">ProtectBkgnds</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-127">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-127">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a4d3-128">ProtectMasters</span><span class="sxs-lookup"><span data-stu-id="9a4d3-128">ProtectMasters</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-129">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-129">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a4d3-130">ProtectShapes</span><span class="sxs-lookup"><span data-stu-id="9a4d3-130">ProtectShapes</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-131">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-131">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a4d3-132">ProtectStyles</span><span class="sxs-lookup"><span data-stu-id="9a4d3-132">ProtectStyles</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-133">ProtectStyles_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-133">ProtectStyles_Type</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a4d3-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="9a4d3-134">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-135">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-135">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a4d3-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="9a4d3-136">SnapExtensions</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-137">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-137">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9a4d3-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="9a4d3-138">SnapSettings</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a4d3-139">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="9a4d3-139">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9a4d3-140">Attributs</span><span class="sxs-lookup"><span data-stu-id="9a4d3-140">Attributes</span></span>

|<span data-ttu-id="9a4d3-141">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9a4d3-141">**Attribute**</span></span>|<span data-ttu-id="9a4d3-142">**Type**</span><span class="sxs-lookup"><span data-stu-id="9a4d3-142">**Type**</span></span>|<span data-ttu-id="9a4d3-143">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="9a4d3-143">**Required**</span></span>|<span data-ttu-id="9a4d3-144">**Description**</span><span class="sxs-lookup"><span data-stu-id="9a4d3-144">**Description**</span></span>|<span data-ttu-id="9a4d3-145">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="9a4d3-145">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9a4d3-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="9a4d3-146">DefaultFillStyle</span></span>  <br/> |<span data-ttu-id="9a4d3-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a4d3-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a4d3-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a4d3-148">optional</span></span>  <br/> ||<span data-ttu-id="9a4d3-149">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a4d3-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a4d3-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="9a4d3-150">DefaultGuideStyle</span></span>  <br/> |<span data-ttu-id="9a4d3-151">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a4d3-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a4d3-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a4d3-152">optional</span></span>  <br/> ||<span data-ttu-id="9a4d3-153">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a4d3-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a4d3-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="9a4d3-154">DefaultLineStyle</span></span>  <br/> |<span data-ttu-id="9a4d3-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a4d3-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a4d3-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a4d3-156">optional</span></span>  <br/> ||<span data-ttu-id="9a4d3-157">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a4d3-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a4d3-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="9a4d3-158">DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="9a4d3-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a4d3-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a4d3-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a4d3-160">optional</span></span>  <br/> ||<span data-ttu-id="9a4d3-161">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a4d3-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a4d3-162">TopPage</span><span class="sxs-lookup"><span data-stu-id="9a4d3-162">TopPage</span></span>  <br/> |<span data-ttu-id="9a4d3-163">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a4d3-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a4d3-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="9a4d3-164">optional</span></span>  <br/> ||<span data-ttu-id="9a4d3-165">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a4d3-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

