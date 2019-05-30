---
title: ComplexType Master_Type (Visio XML)
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
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="19ca1-102">ComplexType Master_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="19ca1-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="19ca1-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="19ca1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19ca1-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="19ca1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="19ca1-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="19ca1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="19ca1-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="19ca1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="19ca1-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="19ca1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="19ca1-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="19ca1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="19ca1-109">Définition</span><span class="sxs-lookup"><span data-stu-id="19ca1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="19ca1-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="19ca1-110">Elements and attributes</span></span>

<span data-ttu-id="19ca1-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="19ca1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="19ca1-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="19ca1-112">Child elements</span></span>

|<span data-ttu-id="19ca1-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="19ca1-113">**Element**</span></span>|<span data-ttu-id="19ca1-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="19ca1-114">**Type**</span></span>|<span data-ttu-id="19ca1-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="19ca1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="19ca1-116">Icon</span><span class="sxs-lookup"><span data-stu-id="19ca1-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19ca1-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="19ca1-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19ca1-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="19ca1-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19ca1-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="19ca1-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19ca1-120">Ver</span><span class="sxs-lookup"><span data-stu-id="19ca1-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19ca1-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="19ca1-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="19ca1-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="19ca1-122">Attributes</span></span>

|<span data-ttu-id="19ca1-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="19ca1-123">**Attribute**</span></span>|<span data-ttu-id="19ca1-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="19ca1-124">**Type**</span></span>|<span data-ttu-id="19ca1-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="19ca1-125">**Required**</span></span>|<span data-ttu-id="19ca1-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="19ca1-126">**Description**</span></span>|<span data-ttu-id="19ca1-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="19ca1-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="19ca1-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="19ca1-128">AlignName</span></span>  <br/> |<span data-ttu-id="19ca1-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="19ca1-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="19ca1-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-130">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-131">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="19ca1-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="19ca1-132">BaseID</span></span>  <br/> |<span data-ttu-id="19ca1-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="19ca1-133">xsd:string</span></span>  <br/> |<span data-ttu-id="19ca1-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-134">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-135">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="19ca1-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="19ca1-136">Hidden</span></span>  <br/> |<span data-ttu-id="19ca1-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="19ca1-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19ca1-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-138">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-139">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="19ca1-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="19ca1-140">IconSize</span></span>  <br/> |<span data-ttu-id="19ca1-141">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="19ca1-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="19ca1-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-142">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-143">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="19ca1-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="19ca1-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="19ca1-145">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="19ca1-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19ca1-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-146">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-147">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="19ca1-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-148">ID</span><span class="sxs-lookup"><span data-stu-id="19ca1-148">ID</span></span>  <br/> |<span data-ttu-id="19ca1-149">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19ca1-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19ca1-150">obligatoire</span><span class="sxs-lookup"><span data-stu-id="19ca1-150">required</span></span>  <br/> ||<span data-ttu-id="19ca1-151">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19ca1-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="19ca1-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="19ca1-153">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="19ca1-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19ca1-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-154">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-155">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="19ca1-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="19ca1-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="19ca1-157">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="19ca1-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19ca1-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-158">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-159">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="19ca1-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="19ca1-160">MasterType</span></span>  <br/> |<span data-ttu-id="19ca1-161">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="19ca1-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="19ca1-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-162">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-163">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="19ca1-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="19ca1-164">MatchByName</span></span>  <br/> |<span data-ttu-id="19ca1-165">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="19ca1-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19ca1-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-166">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-167">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="19ca1-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-168">Nom</span><span class="sxs-lookup"><span data-stu-id="19ca1-168">Name</span></span>  <br/> |<span data-ttu-id="19ca1-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="19ca1-169">xsd:string</span></span>  <br/> |<span data-ttu-id="19ca1-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-170">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-171">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="19ca1-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-172">NameU</span><span class="sxs-lookup"><span data-stu-id="19ca1-172">NameU</span></span>  <br/> |<span data-ttu-id="19ca1-173">xsd: String</span><span class="sxs-lookup"><span data-stu-id="19ca1-173">xsd:string</span></span>  <br/> |<span data-ttu-id="19ca1-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-174">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-175">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="19ca1-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="19ca1-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="19ca1-177">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="19ca1-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="19ca1-178">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-178">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-179">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="19ca1-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-180">Invite</span><span class="sxs-lookup"><span data-stu-id="19ca1-180">Prompt</span></span>  <br/> |<span data-ttu-id="19ca1-181">xsd: String</span><span class="sxs-lookup"><span data-stu-id="19ca1-181">xsd:string</span></span>  <br/> |<span data-ttu-id="19ca1-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-182">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-183">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="19ca1-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19ca1-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="19ca1-184">UniqueID</span></span>  <br/> |<span data-ttu-id="19ca1-185">xsd: String</span><span class="sxs-lookup"><span data-stu-id="19ca1-185">xsd:string</span></span>  <br/> |<span data-ttu-id="19ca1-186">facultatif</span><span class="sxs-lookup"><span data-stu-id="19ca1-186">optional</span></span>  <br/> ||<span data-ttu-id="19ca1-187">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="19ca1-187">Values of the xsd:string type.</span></span>  <br/> |
   

