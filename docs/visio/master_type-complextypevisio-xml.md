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
# <a name="master_type-complextype-visio-xml"></a><span data-ttu-id="44a52-102">Master_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="44a52-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="44a52-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="44a52-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44a52-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="44a52-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="44a52-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="44a52-105">**Schema file**</span></span> <br/> |<span data-ttu-id="44a52-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="44a52-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="44a52-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="44a52-107">**Extension base**</span></span> <br/> |<span data-ttu-id="44a52-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="44a52-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="44a52-109">Définition</span><span class="sxs-lookup"><span data-stu-id="44a52-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="44a52-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="44a52-110">Elements and attributes</span></span>

<span data-ttu-id="44a52-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="44a52-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="44a52-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="44a52-112">Child elements</span></span>

|<span data-ttu-id="44a52-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="44a52-113">**Element**</span></span>|<span data-ttu-id="44a52-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="44a52-114">**Type**</span></span>|<span data-ttu-id="44a52-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="44a52-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="44a52-116">Icon</span><span class="sxs-lookup"><span data-stu-id="44a52-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44a52-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="44a52-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="44a52-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="44a52-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44a52-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="44a52-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="44a52-120">Rel</span><span class="sxs-lookup"><span data-stu-id="44a52-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="44a52-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="44a52-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="44a52-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="44a52-122">Attributes</span></span>

|<span data-ttu-id="44a52-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="44a52-123">**Attribute**</span></span>|<span data-ttu-id="44a52-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="44a52-124">**Type**</span></span>|<span data-ttu-id="44a52-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="44a52-125">**Required**</span></span>|<span data-ttu-id="44a52-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="44a52-126">**Description**</span></span>|<span data-ttu-id="44a52-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="44a52-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="44a52-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="44a52-128">AlignName</span></span>  <br/> |<span data-ttu-id="44a52-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="44a52-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="44a52-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-130">optional</span></span>  <br/> ||<span data-ttu-id="44a52-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="44a52-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="44a52-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="44a52-132">BaseID</span></span>  <br/> |<span data-ttu-id="44a52-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="44a52-133">xsd:string</span></span>  <br/> |<span data-ttu-id="44a52-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-134">optional</span></span>  <br/> ||<span data-ttu-id="44a52-135">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="44a52-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="44a52-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="44a52-136">Hidden</span></span>  <br/> |<span data-ttu-id="44a52-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="44a52-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="44a52-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-138">optional</span></span>  <br/> ||<span data-ttu-id="44a52-139">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="44a52-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="44a52-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="44a52-140">IconSize</span></span>  <br/> |<span data-ttu-id="44a52-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="44a52-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="44a52-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-142">optional</span></span>  <br/> ||<span data-ttu-id="44a52-143">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="44a52-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="44a52-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="44a52-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="44a52-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="44a52-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="44a52-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-146">optional</span></span>  <br/> ||<span data-ttu-id="44a52-147">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="44a52-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="44a52-148">ID</span><span class="sxs-lookup"><span data-stu-id="44a52-148">ID</span></span>  <br/> |<span data-ttu-id="44a52-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="44a52-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="44a52-150">obligatoire</span><span class="sxs-lookup"><span data-stu-id="44a52-150">required</span></span>  <br/> ||<span data-ttu-id="44a52-151">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="44a52-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="44a52-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="44a52-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="44a52-153">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="44a52-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="44a52-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-154">optional</span></span>  <br/> ||<span data-ttu-id="44a52-155">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="44a52-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="44a52-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="44a52-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="44a52-157">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="44a52-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="44a52-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-158">optional</span></span>  <br/> ||<span data-ttu-id="44a52-159">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="44a52-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="44a52-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="44a52-160">MasterType</span></span>  <br/> |<span data-ttu-id="44a52-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="44a52-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="44a52-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-162">optional</span></span>  <br/> ||<span data-ttu-id="44a52-163">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="44a52-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="44a52-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="44a52-164">MatchByName</span></span>  <br/> |<span data-ttu-id="44a52-165">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="44a52-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="44a52-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-166">optional</span></span>  <br/> ||<span data-ttu-id="44a52-167">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="44a52-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="44a52-168">Nom</span><span class="sxs-lookup"><span data-stu-id="44a52-168">Name</span></span>  <br/> |<span data-ttu-id="44a52-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="44a52-169">xsd:string</span></span>  <br/> |<span data-ttu-id="44a52-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-170">optional</span></span>  <br/> ||<span data-ttu-id="44a52-171">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="44a52-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="44a52-172">NameU</span><span class="sxs-lookup"><span data-stu-id="44a52-172">NameU</span></span>  <br/> |<span data-ttu-id="44a52-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="44a52-173">xsd:string</span></span>  <br/> |<span data-ttu-id="44a52-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-174">optional</span></span>  <br/> ||<span data-ttu-id="44a52-175">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="44a52-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="44a52-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="44a52-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="44a52-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="44a52-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="44a52-178">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-178">optional</span></span>  <br/> ||<span data-ttu-id="44a52-179">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="44a52-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="44a52-180">Invite</span><span class="sxs-lookup"><span data-stu-id="44a52-180">Prompt</span></span>  <br/> |<span data-ttu-id="44a52-181">xsd:string</span><span class="sxs-lookup"><span data-stu-id="44a52-181">xsd:string</span></span>  <br/> |<span data-ttu-id="44a52-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-182">optional</span></span>  <br/> ||<span data-ttu-id="44a52-183">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="44a52-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="44a52-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="44a52-184">UniqueID</span></span>  <br/> |<span data-ttu-id="44a52-185">xsd:string</span><span class="sxs-lookup"><span data-stu-id="44a52-185">xsd:string</span></span>  <br/> |<span data-ttu-id="44a52-186">facultatif</span><span class="sxs-lookup"><span data-stu-id="44a52-186">optional</span></span>  <br/> ||<span data-ttu-id="44a52-187">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="44a52-187">Values of the xsd:string type.</span></span>  <br/> |
   

