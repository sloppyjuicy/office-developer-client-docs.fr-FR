---
title: ComplexType Master_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 186099d495849706f68113abb269de4a1f5a2ce7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341803"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="f79d0-102">ComplexType Master_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f79d0-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f79d0-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="f79d0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f79d0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f79d0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f79d0-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f79d0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f79d0-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="f79d0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f79d0-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="f79d0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f79d0-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="f79d0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f79d0-109">Définition</span><span class="sxs-lookup"><span data-stu-id="f79d0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f79d0-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f79d0-110">Elements and attributes</span></span>

<span data-ttu-id="f79d0-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="f79d0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f79d0-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f79d0-112">Child elements</span></span>

|<span data-ttu-id="f79d0-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f79d0-113">**Element**</span></span>|<span data-ttu-id="f79d0-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="f79d0-114">**Type**</span></span>|<span data-ttu-id="f79d0-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="f79d0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f79d0-116">Icon</span><span class="sxs-lookup"><span data-stu-id="f79d0-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f79d0-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="f79d0-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f79d0-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="f79d0-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f79d0-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f79d0-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="f79d0-120">Ver</span><span class="sxs-lookup"><span data-stu-id="f79d0-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f79d0-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="f79d0-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f79d0-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="f79d0-122">Attributes</span></span>

|<span data-ttu-id="f79d0-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f79d0-123">**Attribute**</span></span>|<span data-ttu-id="f79d0-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="f79d0-124">**Type**</span></span>|<span data-ttu-id="f79d0-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f79d0-125">**Required**</span></span>|<span data-ttu-id="f79d0-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="f79d0-126">**Description**</span></span>|<span data-ttu-id="f79d0-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f79d0-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f79d0-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="f79d0-128">AlignName</span></span>  <br/> |<span data-ttu-id="f79d0-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f79d0-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f79d0-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-130">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-131">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f79d0-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="f79d0-132">BaseID</span></span>  <br/> |<span data-ttu-id="f79d0-133">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f79d0-133">xsd:string</span></span>  <br/> |<span data-ttu-id="f79d0-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-134">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-135">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f79d0-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-136">Masqué</span><span class="sxs-lookup"><span data-stu-id="f79d0-136">Hidden</span></span>  <br/> |<span data-ttu-id="f79d0-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="f79d0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f79d0-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-138">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-139">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f79d0-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="f79d0-140">IconSize</span></span>  <br/> |<span data-ttu-id="f79d0-141">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f79d0-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f79d0-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-142">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-143">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f79d0-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="f79d0-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="f79d0-145">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="f79d0-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f79d0-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-146">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-147">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f79d0-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-148">ID</span><span class="sxs-lookup"><span data-stu-id="f79d0-148">ID</span></span>  <br/> |<span data-ttu-id="f79d0-149">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f79d0-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f79d0-150">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f79d0-150">required</span></span>  <br/> ||<span data-ttu-id="f79d0-151">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f79d0-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="f79d0-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="f79d0-153">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="f79d0-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f79d0-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-154">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-155">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f79d0-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="f79d0-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="f79d0-157">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="f79d0-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f79d0-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-158">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-159">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f79d0-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="f79d0-160">MasterType</span></span>  <br/> |<span data-ttu-id="f79d0-161">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f79d0-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f79d0-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-162">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-163">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f79d0-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="f79d0-164">MatchByName</span></span>  <br/> |<span data-ttu-id="f79d0-165">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="f79d0-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f79d0-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-166">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-167">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f79d0-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-168">Nom</span><span class="sxs-lookup"><span data-stu-id="f79d0-168">Name</span></span>  <br/> |<span data-ttu-id="f79d0-169">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f79d0-169">xsd:string</span></span>  <br/> |<span data-ttu-id="f79d0-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-170">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-171">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f79d0-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-172">NameU</span><span class="sxs-lookup"><span data-stu-id="f79d0-172">NameU</span></span>  <br/> |<span data-ttu-id="f79d0-173">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f79d0-173">xsd:string</span></span>  <br/> |<span data-ttu-id="f79d0-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-174">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-175">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f79d0-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="f79d0-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="f79d0-177">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f79d0-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f79d0-178">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-178">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-179">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f79d0-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-180">Invite</span><span class="sxs-lookup"><span data-stu-id="f79d0-180">Prompt</span></span>  <br/> |<span data-ttu-id="f79d0-181">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f79d0-181">xsd:string</span></span>  <br/> |<span data-ttu-id="f79d0-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-182">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-183">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f79d0-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f79d0-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="f79d0-184">UniqueID</span></span>  <br/> |<span data-ttu-id="f79d0-185">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f79d0-185">xsd:string</span></span>  <br/> |<span data-ttu-id="f79d0-186">facultatif</span><span class="sxs-lookup"><span data-stu-id="f79d0-186">optional</span></span>  <br/> ||<span data-ttu-id="f79d0-187">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f79d0-187">Values of the xsd:string type.</span></span>  <br/> |
   

