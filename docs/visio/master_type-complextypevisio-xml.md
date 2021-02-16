---
title: Master_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 22b619149fc5393f085ca6e245c65ed6058538ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538066"
---
# <a name="master_type-complextype-visio-xml"></a><span data-ttu-id="c16a8-102">Master_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c16a8-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c16a8-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c16a8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c16a8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c16a8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c16a8-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c16a8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c16a8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c16a8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c16a8-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c16a8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c16a8-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="c16a8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c16a8-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c16a8-109">Definition</span></span>

```XML
          <xs:complexType name="Master_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="BaseID"
  type="xsd:string"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="MatchByName"
  type="xsd:boolean"
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
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="Hidden"
  type="xsd:boolean"
    />
    <xs:attribute name="IconUpdate"
  type="xsd:boolean"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c16a8-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c16a8-110">Elements and attributes</span></span>

<span data-ttu-id="c16a8-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="c16a8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c16a8-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c16a8-112">Child elements</span></span>

|<span data-ttu-id="c16a8-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c16a8-113">**Element**</span></span>|<span data-ttu-id="c16a8-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c16a8-114">**Type**</span></span>|<span data-ttu-id="c16a8-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="c16a8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c16a8-116">Icon</span><span class="sxs-lookup"><span data-stu-id="c16a8-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c16a8-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="c16a8-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c16a8-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="c16a8-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c16a8-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="c16a8-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c16a8-120">Rel</span><span class="sxs-lookup"><span data-stu-id="c16a8-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c16a8-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="c16a8-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c16a8-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="c16a8-122">Attributes</span></span>

|<span data-ttu-id="c16a8-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c16a8-123">**Attribute**</span></span>|<span data-ttu-id="c16a8-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="c16a8-124">**Type**</span></span>|<span data-ttu-id="c16a8-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c16a8-125">**Required**</span></span>|<span data-ttu-id="c16a8-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="c16a8-126">**Description**</span></span>|<span data-ttu-id="c16a8-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c16a8-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c16a8-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="c16a8-128">AlignName</span></span>  <br/> |<span data-ttu-id="c16a8-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c16a8-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c16a8-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-130">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c16a8-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="c16a8-132">BaseID</span></span>  <br/> |<span data-ttu-id="c16a8-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c16a8-133">xsd:string</span></span>  <br/> |<span data-ttu-id="c16a8-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-134">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c16a8-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="c16a8-136">Hidden</span></span>  <br/> |<span data-ttu-id="c16a8-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c16a8-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c16a8-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-138">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-139">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c16a8-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="c16a8-140">IconSize</span></span>  <br/> |<span data-ttu-id="c16a8-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c16a8-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c16a8-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-142">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-143">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c16a8-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="c16a8-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="c16a8-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c16a8-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c16a8-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-146">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-147">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c16a8-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-148">ID</span><span class="sxs-lookup"><span data-stu-id="c16a8-148">ID</span></span>  <br/> |<span data-ttu-id="c16a8-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c16a8-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c16a8-150">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c16a8-150">required</span></span>  <br/> ||<span data-ttu-id="c16a8-151">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c16a8-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="c16a8-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="c16a8-153">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c16a8-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c16a8-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-154">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-155">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c16a8-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="c16a8-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="c16a8-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c16a8-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c16a8-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-158">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-159">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c16a8-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="c16a8-160">MasterType</span></span>  <br/> |<span data-ttu-id="c16a8-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c16a8-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c16a8-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-162">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-163">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c16a8-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="c16a8-164">MatchByName</span></span>  <br/> |<span data-ttu-id="c16a8-165">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c16a8-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c16a8-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-166">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-167">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c16a8-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-168">Nom</span><span class="sxs-lookup"><span data-stu-id="c16a8-168">Name</span></span>  <br/> |<span data-ttu-id="c16a8-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c16a8-169">xsd:string</span></span>  <br/> |<span data-ttu-id="c16a8-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-170">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-171">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c16a8-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-172">NameU</span><span class="sxs-lookup"><span data-stu-id="c16a8-172">NameU</span></span>  <br/> |<span data-ttu-id="c16a8-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c16a8-173">xsd:string</span></span>  <br/> |<span data-ttu-id="c16a8-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-174">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-175">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c16a8-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="c16a8-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="c16a8-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c16a8-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c16a8-178">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-178">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-179">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c16a8-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-180">Invite</span><span class="sxs-lookup"><span data-stu-id="c16a8-180">Prompt</span></span>  <br/> |<span data-ttu-id="c16a8-181">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c16a8-181">xsd:string</span></span>  <br/> |<span data-ttu-id="c16a8-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-182">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-183">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c16a8-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c16a8-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="c16a8-184">UniqueID</span></span>  <br/> |<span data-ttu-id="c16a8-185">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c16a8-185">xsd:string</span></span>  <br/> |<span data-ttu-id="c16a8-186">facultatif</span><span class="sxs-lookup"><span data-stu-id="c16a8-186">optional</span></span>  <br/> ||<span data-ttu-id="c16a8-187">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c16a8-187">Values of the xsd:string type.</span></span>  <br/> |
   

