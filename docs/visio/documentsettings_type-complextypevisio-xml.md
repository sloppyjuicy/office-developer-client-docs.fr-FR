---
title: Type complexe DocumentSettings_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 704591a2bf03f3eaf4d93b167475a8bae286da3e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384674"
---
# <a name="documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="383e4-102">Type complexe DocumentSettings_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="383e4-102">DocumentSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="383e4-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="383e4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="383e4-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="383e4-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="383e4-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="383e4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="383e4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="383e4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="383e4-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="383e4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="383e4-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="383e4-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="383e4-109">Définition</span><span class="sxs-lookup"><span data-stu-id="383e4-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="383e4-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="383e4-110">Elements and attributes</span></span>

<span data-ttu-id="383e4-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="383e4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="383e4-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="383e4-112">Child elements</span></span>

|<span data-ttu-id="383e4-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="383e4-113">**Element**</span></span>|<span data-ttu-id="383e4-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="383e4-114">**Type**</span></span>|<span data-ttu-id="383e4-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="383e4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="383e4-116">AttachedToolbars</span><span class="sxs-lookup"><span data-stu-id="383e4-116">AttachedToolbars</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-117">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-117">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="383e4-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="383e4-118">CustomMenusFile</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-119">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-119">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="383e4-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="383e4-120">CustomToolbarsFile</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-121">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-121">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="383e4-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="383e4-122">DynamicGridEnabled</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-123">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-123">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="383e4-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="383e4-124">GlueSettings</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-125">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-125">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="383e4-126">ProtectBkgnds</span><span class="sxs-lookup"><span data-stu-id="383e4-126">ProtectBkgnds</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-127">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-127">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="383e4-128">ProtectMasters</span><span class="sxs-lookup"><span data-stu-id="383e4-128">ProtectMasters</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-129">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-129">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="383e4-130">ProtectShapes</span><span class="sxs-lookup"><span data-stu-id="383e4-130">ProtectShapes</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-131">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-131">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="383e4-132">ProtectStyles</span><span class="sxs-lookup"><span data-stu-id="383e4-132">ProtectStyles</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-133">ProtectStyles_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-133">ProtectStyles_Type</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="383e4-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="383e4-134">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-135">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-135">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="383e4-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="383e4-136">SnapExtensions</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-137">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-137">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="383e4-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="383e4-138">SnapSettings</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="383e4-139">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="383e4-139">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="383e4-140">Attributs</span><span class="sxs-lookup"><span data-stu-id="383e4-140">Attributes</span></span>

|<span data-ttu-id="383e4-141">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="383e4-141">**Attribute**</span></span>|<span data-ttu-id="383e4-142">**Type**</span><span class="sxs-lookup"><span data-stu-id="383e4-142">**Type**</span></span>|<span data-ttu-id="383e4-143">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="383e4-143">**Required**</span></span>|<span data-ttu-id="383e4-144">**Description**</span><span class="sxs-lookup"><span data-stu-id="383e4-144">**Description**</span></span>|<span data-ttu-id="383e4-145">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="383e4-145">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="383e4-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="383e4-146">DefaultFillStyle</span></span>  <br/> |<span data-ttu-id="383e4-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="383e4-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="383e4-148">facultatif</span><span class="sxs-lookup"><span data-stu-id="383e4-148">optional</span></span>  <br/> ||<span data-ttu-id="383e4-149">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="383e4-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="383e4-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="383e4-150">DefaultGuideStyle</span></span>  <br/> |<span data-ttu-id="383e4-151">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="383e4-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="383e4-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="383e4-152">optional</span></span>  <br/> ||<span data-ttu-id="383e4-153">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="383e4-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="383e4-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="383e4-154">DefaultLineStyle</span></span>  <br/> |<span data-ttu-id="383e4-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="383e4-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="383e4-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="383e4-156">optional</span></span>  <br/> ||<span data-ttu-id="383e4-157">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="383e4-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="383e4-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="383e4-158">DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="383e4-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="383e4-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="383e4-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="383e4-160">optional</span></span>  <br/> ||<span data-ttu-id="383e4-161">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="383e4-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="383e4-162">TopPage</span><span class="sxs-lookup"><span data-stu-id="383e4-162">TopPage</span></span>  <br/> |<span data-ttu-id="383e4-163">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="383e4-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="383e4-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="383e4-164">optional</span></span>  <br/> ||<span data-ttu-id="383e4-165">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="383e4-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

