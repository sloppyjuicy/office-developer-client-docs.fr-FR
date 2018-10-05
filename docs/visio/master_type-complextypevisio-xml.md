---
title: Type complexe Master_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 186099d495849706f68113abb269de4a1f5a2ce7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397709"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="5dbcb-102">Type complexe Master_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="5dbcb-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5dbcb-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="5dbcb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5dbcb-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="5dbcb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5dbcb-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="5dbcb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5dbcb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5dbcb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5dbcb-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="5dbcb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5dbcb-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="5dbcb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5dbcb-109">Définition</span><span class="sxs-lookup"><span data-stu-id="5dbcb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="5dbcb-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="5dbcb-110">Elements and attributes</span></span>

<span data-ttu-id="5dbcb-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5dbcb-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5dbcb-112">Child elements</span></span>

|<span data-ttu-id="5dbcb-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5dbcb-113">**Element**</span></span>|<span data-ttu-id="5dbcb-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="5dbcb-114">**Type**</span></span>|<span data-ttu-id="5dbcb-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="5dbcb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5dbcb-116">Icône</span><span class="sxs-lookup"><span data-stu-id="5dbcb-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5dbcb-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="5dbcb-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5dbcb-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="5dbcb-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5dbcb-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="5dbcb-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="5dbcb-120">Rel</span><span class="sxs-lookup"><span data-stu-id="5dbcb-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5dbcb-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="5dbcb-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5dbcb-122">Attributs</span><span class="sxs-lookup"><span data-stu-id="5dbcb-122">Attributes</span></span>

|<span data-ttu-id="5dbcb-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5dbcb-123">**Attribute**</span></span>|<span data-ttu-id="5dbcb-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="5dbcb-124">**Type**</span></span>|<span data-ttu-id="5dbcb-125">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="5dbcb-125">**Required**</span></span>|<span data-ttu-id="5dbcb-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="5dbcb-126">**Description**</span></span>|<span data-ttu-id="5dbcb-127">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="5dbcb-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5dbcb-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="5dbcb-128">AlignName</span></span>  <br/> |<span data-ttu-id="5dbcb-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="5dbcb-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="5dbcb-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-130">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="5dbcb-132">BaseID</span></span>  <br/> |<span data-ttu-id="5dbcb-133">XSD : String</span><span class="sxs-lookup"><span data-stu-id="5dbcb-133">xsd:string</span></span>  <br/> |<span data-ttu-id="5dbcb-134">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-134">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-135">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="5dbcb-136">Hidden</span></span>  <br/> |<span data-ttu-id="5dbcb-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="5dbcb-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5dbcb-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-138">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-139">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="5dbcb-140">IconSize</span></span>  <br/> |<span data-ttu-id="5dbcb-141">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="5dbcb-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="5dbcb-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-142">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-143">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="5dbcb-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="5dbcb-145">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="5dbcb-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5dbcb-146">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-146">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-147">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-148">ID</span><span class="sxs-lookup"><span data-stu-id="5dbcb-148">ID</span></span>  <br/> |<span data-ttu-id="5dbcb-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5dbcb-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5dbcb-150">obligatoire</span><span class="sxs-lookup"><span data-stu-id="5dbcb-150">required</span></span>  <br/> ||<span data-ttu-id="5dbcb-151">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="5dbcb-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="5dbcb-153">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="5dbcb-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5dbcb-154">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-154">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-155">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="5dbcb-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="5dbcb-157">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="5dbcb-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5dbcb-158">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-158">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-159">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="5dbcb-160">MasterType</span></span>  <br/> |<span data-ttu-id="5dbcb-161">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="5dbcb-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="5dbcb-162">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-162">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-163">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="5dbcb-164">MatchByName</span></span>  <br/> |<span data-ttu-id="5dbcb-165">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="5dbcb-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="5dbcb-166">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-166">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-167">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-168">Nom</span><span class="sxs-lookup"><span data-stu-id="5dbcb-168">Name</span></span>  <br/> |<span data-ttu-id="5dbcb-169">XSD : String</span><span class="sxs-lookup"><span data-stu-id="5dbcb-169">xsd:string</span></span>  <br/> |<span data-ttu-id="5dbcb-170">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-170">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-171">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-172">NameU</span><span class="sxs-lookup"><span data-stu-id="5dbcb-172">NameU</span></span>  <br/> |<span data-ttu-id="5dbcb-173">XSD : String</span><span class="sxs-lookup"><span data-stu-id="5dbcb-173">xsd:string</span></span>  <br/> |<span data-ttu-id="5dbcb-174">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-174">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-175">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="5dbcb-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="5dbcb-177">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="5dbcb-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="5dbcb-178">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-178">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-179">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="5dbcb-180">Prompt</span></span>  <br/> |<span data-ttu-id="5dbcb-181">XSD : String</span><span class="sxs-lookup"><span data-stu-id="5dbcb-181">xsd:string</span></span>  <br/> |<span data-ttu-id="5dbcb-182">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-182">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-183">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="5dbcb-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="5dbcb-184">UniqueID</span></span>  <br/> |<span data-ttu-id="5dbcb-185">XSD : String</span><span class="sxs-lookup"><span data-stu-id="5dbcb-185">xsd:string</span></span>  <br/> |<span data-ttu-id="5dbcb-186">facultatif</span><span class="sxs-lookup"><span data-stu-id="5dbcb-186">optional</span></span>  <br/> ||<span data-ttu-id="5dbcb-187">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="5dbcb-187">Values of the xsd:string type.</span></span>  <br/> |
   

