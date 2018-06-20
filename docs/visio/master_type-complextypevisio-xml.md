---
title: Type complexe Master_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: b4dde4d00552525a5ec17116f96151f39c6d0957
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789066"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="0016d-102">Type complexe Master_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="0016d-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0016d-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="0016d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0016d-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="0016d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0016d-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0016d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0016d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0016d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0016d-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="0016d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0016d-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="0016d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0016d-109">Définition</span><span class="sxs-lookup"><span data-stu-id="0016d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0016d-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0016d-110">Elements and attributes</span></span>

<span data-ttu-id="0016d-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="0016d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0016d-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0016d-112">Child elements</span></span>

|<span data-ttu-id="0016d-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0016d-113">**Element**</span></span>|<span data-ttu-id="0016d-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="0016d-114">**Type**</span></span>|<span data-ttu-id="0016d-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="0016d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0016d-116">Icône</span><span class="sxs-lookup"><span data-stu-id="0016d-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0016d-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="0016d-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0016d-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="0016d-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0016d-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="0016d-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0016d-120">Rel</span><span class="sxs-lookup"><span data-stu-id="0016d-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0016d-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="0016d-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0016d-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="0016d-122">Attributes</span></span>

|<span data-ttu-id="0016d-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0016d-123">**Attribute**</span></span>|<span data-ttu-id="0016d-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="0016d-124">**Type**</span></span>|<span data-ttu-id="0016d-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="0016d-125">**Required**</span></span>|<span data-ttu-id="0016d-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="0016d-126">**Description**</span></span>|<span data-ttu-id="0016d-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="0016d-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0016d-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="0016d-128">AlignName</span></span>  <br/> |<span data-ttu-id="0016d-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="0016d-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0016d-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-130">optional</span></span>  <br/> ||<span data-ttu-id="0016d-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="0016d-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0016d-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="0016d-132">BaseID</span></span>  <br/> |<span data-ttu-id="0016d-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="0016d-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0016d-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-134">optional</span></span>  <br/> ||<span data-ttu-id="0016d-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="0016d-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0016d-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="0016d-136">Hidden</span></span>  <br/> |<span data-ttu-id="0016d-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="0016d-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0016d-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-138">optional</span></span>  <br/> ||<span data-ttu-id="0016d-139">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="0016d-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0016d-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="0016d-140">IconSize</span></span>  <br/> |<span data-ttu-id="0016d-141">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="0016d-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0016d-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-142">optional</span></span>  <br/> ||<span data-ttu-id="0016d-143">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="0016d-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0016d-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="0016d-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="0016d-145">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="0016d-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0016d-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-146">optional</span></span>  <br/> ||<span data-ttu-id="0016d-147">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="0016d-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0016d-148">ID</span><span class="sxs-lookup"><span data-stu-id="0016d-148">ID</span></span>  <br/> |<span data-ttu-id="0016d-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0016d-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0016d-150">obligatoire</span><span class="sxs-lookup"><span data-stu-id="0016d-150">required</span></span>  <br/> ||<span data-ttu-id="0016d-151">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0016d-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0016d-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="0016d-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="0016d-153">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="0016d-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0016d-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-154">optional</span></span>  <br/> ||<span data-ttu-id="0016d-155">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="0016d-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0016d-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="0016d-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="0016d-157">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="0016d-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0016d-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-158">optional</span></span>  <br/> ||<span data-ttu-id="0016d-159">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="0016d-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0016d-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="0016d-160">MasterType</span></span>  <br/> |<span data-ttu-id="0016d-161">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="0016d-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0016d-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-162">optional</span></span>  <br/> ||<span data-ttu-id="0016d-163">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="0016d-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0016d-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="0016d-164">MatchByName</span></span>  <br/> |<span data-ttu-id="0016d-165">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="0016d-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0016d-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-166">optional</span></span>  <br/> ||<span data-ttu-id="0016d-167">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="0016d-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0016d-168">Nom</span><span class="sxs-lookup"><span data-stu-id="0016d-168">Name</span></span>  <br/> |<span data-ttu-id="0016d-169">XSD : String</span><span class="sxs-lookup"><span data-stu-id="0016d-169">xsd:string</span></span>  <br/> |<span data-ttu-id="0016d-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-170">optional</span></span>  <br/> ||<span data-ttu-id="0016d-171">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="0016d-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0016d-172">NameU</span><span class="sxs-lookup"><span data-stu-id="0016d-172">NameU</span></span>  <br/> |<span data-ttu-id="0016d-173">XSD : String</span><span class="sxs-lookup"><span data-stu-id="0016d-173">xsd:string</span></span>  <br/> |<span data-ttu-id="0016d-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-174">optional</span></span>  <br/> ||<span data-ttu-id="0016d-175">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="0016d-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0016d-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="0016d-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="0016d-177">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="0016d-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0016d-178">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-178">optional</span></span>  <br/> ||<span data-ttu-id="0016d-179">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="0016d-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0016d-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="0016d-180">Prompt</span></span>  <br/> |<span data-ttu-id="0016d-181">XSD : String</span><span class="sxs-lookup"><span data-stu-id="0016d-181">xsd:string</span></span>  <br/> |<span data-ttu-id="0016d-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-182">optional</span></span>  <br/> ||<span data-ttu-id="0016d-183">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="0016d-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0016d-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="0016d-184">UniqueID</span></span>  <br/> |<span data-ttu-id="0016d-185">XSD : String</span><span class="sxs-lookup"><span data-stu-id="0016d-185">xsd:string</span></span>  <br/> |<span data-ttu-id="0016d-186">facultatif</span><span class="sxs-lookup"><span data-stu-id="0016d-186">optional</span></span>  <br/> ||<span data-ttu-id="0016d-187">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="0016d-187">Values of the xsd:string type.</span></span>  <br/> |
   

